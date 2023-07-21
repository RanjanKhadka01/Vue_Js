
<template>
  <div>
    <pre>
      {{ JSON.stringify(fromValue, null, 2) }}
    </pre>
  </div>

<form @submit="submitForm">
  <div>
    <label for="name">Name</label>
    <input type="text" id="name" v-model="fromValue.name">
  </div>
<br>
  <div>
    <label for="profile">Profile Summary</label>
    <textarea id="profile" v-model="fromValue.profile"/>
  </div>

<div>
  <label for="country">Country</label>
  <select id="country" v-model="fromValue.country">
    <option value="">Select a Country</option>
    <option value="nepal">Nepal</option>
    <option value="usa">USA</option>
    <option value="canada">Canada</option>
  </select>
</div>
<br>
<div>
  <label for="job-location">Job Location </label>
  <select id="job-location" multiple v-model="fromValue.jobLocation">
    <option value="nepal">Nepal</option>
    <option value="usa">USA</option>
    <option value="canada">Canada</option>
    <option value="australia">Australia</option>
  </select>
</div>

<div>
  <input type="checkbox" name="remoteJob" v-model="fromValue.remoteJob"/>
  <label for="remoteJob">Open to remote work?</label>
</div>

<div>
  <input type="checkbox" name="remoteJob" v-model="fromValue.transportation"
  true-value="yes"
  false-value="no"/>
  <label for="remoteJob">Need Transportation ?</label>
</div>

<div>
  <label for="">Skill Set: </label>
  <input type="checkbox" id="html" value="html" v-model="fromValue.skillSet"/>
  <label for="html">HTML</label>
  <input type="checkbox" id="css" value="css" v-model="fromValue.skillSet"/>
  <label for="css">CSS</label>
  <input type="checkbox" id="js" value="js" v-model="fromValue.skillSet"/>
  <label for="js">JavaScript</label>
</div>

<div>
  <label for="">Years of Experience</label>
  <input type="radio" id="0-2" value="0-2" v-model="fromValue.yearsOfExperience"/>

  <label for="0-2">0-2</label>
  <input type="radio" id="3-5" value="3-5" v-model="fromValue.yearsOfExperience"/>

  <label for="3-5">3-5</label>
  <input type="radio" id="6-10" value="6-10" v-model="fromValue.yearsOfExperience"/>

  <label for="6-10">6-10</label>
  <input type="radio" id="10+" value="10+" v-model="fromValue.yearsOfExperience"/>
  <label for="6-10">10+</label>

  <div>
    <button>Submit</button>
  </div>

</div>

</form>


</template>


<script>



export default {
  name: 'App',
  data() {
    return {
      fromValue: {
        name: '',
        profile: '',
        country: '',
        jobLocation: [],
        remoteJob: false,
        transportation: 'no',
        skillSet: [],
        yearsOfExperience: '',

      }
      }
    },
    methods: {
      submitForm(event) {
        event.preventDefault()
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
