<template>
</template>


<script>
import Pusher from 'pusher-js'

export default {
  name: 'IndexPage'

  mounted(){
     Pusher.logToConsole = true;

    const pusher = new Pusher('18e45999a252e4b40575', {
      cluster: 'eu'
    });

    const channel = pusher.subscribe('my-channel');
    channel.bind('my-event', function(data) {
      app.messages.push(JSON.stringify(data));
    });

  }

  methods: {
    clickon(){

    }
  }

}
</script>
