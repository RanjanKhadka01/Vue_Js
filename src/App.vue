
<template>
<div>
  {{ greet }} {{ name }}
</div>
<div v-html="company"></div>
<div v-html="hack"></div>
<h2 v-bind:id="headingId">Heading</h2>
<button v-bind:disabled="isDisabled">Bind</button>
<div class="underline">Lorem ipsum dolor sit amet</div>
<div class="unserline" v-bind:class="status">Lorem, ipsum dolor.</div>
<div v-bind:class="isPromoted && 'promoted' ">Promote Movie</div>

<div v-bind:class="isSoldout ? 'soldout' : 'new'">Movie Sold Out</div>

<h2 v-bind:class="['new','promoted']">Newly Promoted</h2>

<h2 v-bind:class="{
  promoted: isPromoted,
  new: !soldout,
  'soldout': isSoldout
}">
Object Conditional
</h2>

<h2 v-bind:style="{
  color: highlight,
  fontSize: headerSize + 'px'
}">Inline Style</h2>

<h2 :style="styleObj">New CSS style</h2>

<div :style="[baseStyleObject,successStyleObject]">Array Style</div>




</template>


<script>

import { ref } from 'vue';

export default {
  name: 'App',
  data() {
    return {
      greet: 'Hello',
      name: 'Dadey',
      company: '<b>Ambition Guru<b>',
      hack: `<a href="#" onclick="alert('You have been hacked')">Win a prize!</a>`,
      headingId: 'heading',
      isDisabled: true,
      status: 'danger',
      isPromoted: true,
      isSoldout: false,
      highlight: 'blue',
      headerSize: 50,
      styleObj: {
        color: 'red',
        fontSize: '50px',
        padidng: '20px',
      },
      baseStyleObject: {
        fontSize: '50px',
        padidng: '10px',
      },
      successStyleObject: {
        color: 'green',
        backgroundColor: 'lightgreen',
        border: '1px solid green',

      },
    };
  },
};
</script>



<style>

#app {
  text-align: center;
  margin-top: 60px;
}

.underline {
  text-decoration: underline dashed;
}

.promoted {
  font-style: italic;
  font-weight: bold;
}

.soldout{
  color: red;
}

.new{
  color: green;
}
</style>
