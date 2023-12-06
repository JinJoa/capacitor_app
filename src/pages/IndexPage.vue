<template>
  <q-page class="flex flex-center">
    hello word!
    <q-btn
      icon="location_on"
      label="GPS"
      @click="$router.push('/gps')"
    />
    <q-btn
      icon="photo_camera"
      label="Camera"
      @click="$router.push('/camera')"
    />
    <q-btn
      icon="smartphone"
      label="Device"
      @click="$router.push('/device')"
    />
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage'
})
</script>
