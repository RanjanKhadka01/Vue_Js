
<template>
<h2 v-for="(name, index) in names" :key="name">{{index}} {{name}}</h2>

<h2 v-for="name in fullNames" :key="fullname">{{name.first}} {{name.last}}</h2>

<div v-for="actor in actors" :key="actor.movies">
  <h2>{{actor.name}}</h2>
  <h3 v-for="movie in actor.movies">{{movie}}</h3>
</div>

<template v-for="(info,key, index) in myinfo" :key="info">
  <h3>
   {{ index }} {{ key }} {{ info }}
  </h3>
</template>
</template>


<script>


export default {
  name: 'App',
  data() {
    return {
      names: ['Dadey', 'Vanja', 'Gothey'],

      fullNames: [
        {first: 'Vanja', last: 'Puir'},
        {first: 'Dadey', last: 'Mujurmuti'},
        {first: 'Dhimal', last: 'Bbek'},
      ],

      actors: [
        {
          name: 'Christian Bale',
          movies: ['Batman', 'The Prestiage'],
        },
        {
          name: 'Di Caprio',
          movies: ['Titanic', 'Inception'],
        },
      ],

      myinfo: {
        name: 'Murra',
        desination: 'QA',
        company: 'AG',
      }
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
