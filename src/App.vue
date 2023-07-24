
<template>
<Greet name="Dadey" hero-name="Umaga"/>
<Greet name="Murra" hero-name="Rusev"/>
<Greet :name="name" :hero-name="address"/>
</template>

<script>
import Greet from './components/Greet.vue'
export default {
  name: 'App',
  components: {
    Greet,
  },
  data() {
    return {
      name: 'Vanja',
      address: 'Old Baneshwor',
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



<!-- In Vue.js, props are a way to pass data from a parent component (the one that contains the child component) to a child component (the one being included or used within the parent component). This allows you to create reusable components with dynamic data, making your application more modular and maintainable.

To use props in Vue.js, you define them as attributes on the custom component's tag in the parent component's template. Then, you can access these props in the child component using the props option.

 -->