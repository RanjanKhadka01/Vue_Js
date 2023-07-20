
<template>
<h2 v-if=" num == 0">The number is zero</h2>
<h2 v-else-if=" num < 0">The number is negative</h2>
<h2 v-else-if=" num > 0">The number is positive</h2>
<h2 v-else>Not a number</h2>

<template v-if="display">
  <h2>Hello</h2>
  <h2>World</h2>
</template>

<h2 v-show="element">V Show</h2>  <!--It is always present in DOM despite negative expression. It only change CSS properties to display:none-->
<h2 v-if="element">V IF</h2> <!--It remove element from the DOM if the expression evaluate to false-->

</template>


<script>


export default {
  name: 'App',
  data() {
    return {
      num : 10,

      display: true,

      element: true
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
