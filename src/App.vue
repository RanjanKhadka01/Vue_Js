
<template>
<h2>Volume 0-20</h2>
<h3>Volume: {{volume}}</h3>
<button @click="volume +=2">Increase Volume</button>
<button @click="volume -=2">Decrease Volume</button>


</template>

<script>



export default {
  name: 'App',
  data() {
    return {
      volume: 0,

      }
    },
    methods: {
    },

    computed: {
    },

    watch: {
      volume(newData, oldData) {
        if(newData > oldData && newData == 16){
          alert('Listening to a high volume may damage your hearing capacity')
        }
      }
    }
  }

</script>



<style>

#app {
  text-align: center;
  margin-top: 60px;
}

</style>
