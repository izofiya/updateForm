<template>
  <div class="container">
    <h1>{{ msg }}</h1>
    <Progress msg="Please fill out the form"></Progress>
    <form v-on:submit.prevent="onSubmit">
      <TotalInformation msg="Total information"></TotalInformation>
      <Education msg="Education"></Education>
      <ContactInformation msg="Contact Information"></ContactInformation>
      <UploadPhoto msg="Upload a photo"></UploadPhoto>
      <input type="submit" v-model="Submit">
    </form>
    <div class="info">
      <ul>
        <li>{{inputs[0]}}</li>
      </ul>
    </div>
  </div>
</template>
<script>
import Progress from './Progress'
import TotalInformation from './TotalInformation'
import Education from './Education'
import ContactInformation from './ContactInformation'
import UploadPhoto from './UploadPhoto'
export default {
    data() {
        return {
            msg: 'Form to fill',
            inputs: [],
        }
    },
    methods: {
        onSubmit: function() {
            this.inputs.push('someValueInput')
        },
    },
    components: {
        Progress: Progress,
        TotalInformation: TotalInformation,
        Education: Education,
        ContactInformation: ContactInformation,
        UploadPhoto: UploadPhoto,
    },
}
</script>
<style>
.container {
    color: rgb(94, 4, 4);
}
</style>

