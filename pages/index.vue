<template>
  <div class="container">
    <button id="button" @click='sendMessage'>Send message</button>
  </div>
</template>


<script>
import Pusher from 'pusher-js'

export default {
  methods: {
    sendMessage() {
      console.log("hello")

    }
  }
}

</script>
