
<template>

<h2>fullName: {{firstName}} {{lastName}}</h2>
 <h2>Computed FullName: {{fullName}}</h2>
<button @click="items.push({id:4, title: 'Keyboard', price:50})">Add Item</button>
<h2>Computed Total : {{total}}</h2>
<h2>Methods Total : {{getTotal()}}</h2>

<input type="text" v-model="country">

<template v-for="item in items" :key="item.id">
<h2 v-if="item.price >= 100">{{item.name}} : {{item.price}}</h2>
</template>

<!-- <h2 v-for="item in expensiveItem" :key="item.id">
  {{ item.name }}  {{ item.price }}
</h2> -->

<button @click="changeName()">Change Name</button>

</template>

<script>



export default {
  name: 'App',
  data() {
    return {
      firstName: 'Murra',
      lastName: 'dadey',

      items: [
        {
          id: 1,
          name: 'apple',
          price: 100,
        },
        {
          id: 2,
          name: 'mango',
          price: 150,
        },
        {
          id: 3,
          name: 'banana',
          price: 50,
        },
      ],
      country: ''
      }
    },
    methods: {
      getTotal() {
        return this.items.reduce((total, curr) => (total = total + curr.price), 0)
      },
      changeName() {
        this.fullName = 'Dadey Mungrati'
      }
    },

    computed: {
      fullName: {
        get() {
        return `${this.firstName} ${this.lastName}`
        },
        set(value) {
          const names = value.split(' ')
          this.firstName = names[0]
          this.lastName = names[1]

        }
      },
      total() {
        return this.items.reduce((total, curr) => (total = total + curr.price), 0)
      },
      expensiveItem() {
        return $this.items.filter(item => item.price > 100)
      },
    },
  }

</script>



<style>

#app {
  text-align: center;
  margin-top: 60px;
}

</style>
