
<template>
  <template v-for="name in names" :key="name">
  <h2 v-if="name == 'vanja'">  {{name}} </h2>
  </template>

</template>


<script>


export default {
  name: 'App',
  data() {
    return {
      names: ['vanja', 'murra', 'umaga', 'mujurmati'],
      }
    },
  }

</script>



<style>

#app {
  text-align: center;
  margin-top: 60px;
}

</style>
