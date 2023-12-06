<template>
  <div>
    <div>Model: {{ model }}</div>
    <div>Manufacturer: {{ manufacturer }}</div>
  </div>
</template>

<script>
import { ref, onMounted } from 'vue'
import { Device } from '@capacitor/device'

export default {
  setup () {
    const model = ref('Please wait...')
    const manufacturer = ref('Please wait...')

    onMounted(() => {
      Device.getInfo().then(info => {
        model.value = info.model
        manufacturer.value = info.manufacturer
      })
    })

    return {
      model,
      manufacturer
    }
  }
}
</script>
