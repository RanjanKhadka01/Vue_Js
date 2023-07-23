
<template>
<div>
 <h2 v-once>{{name}}</h2> <!--element in v-once only evaluate and render once-->
  <button @click="name = 'Murra'">Change Name</button> <!--v-pre tell vue to skip the compilation process element and its children-->

  <h2 v-pre>{{name}}</h2>
</div>

</template>


<script>



export default {
  name: 'App',
  data() {
    return {
     name: 'dadey',
      }
    },
    methods: {
      submitForm(event) {
        console.log('Form Values', this.fromValue)
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
