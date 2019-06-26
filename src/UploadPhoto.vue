<template>
    <fieldset>
        <legend>{{msg}}</legend>
        <input id="inputImg" type='file' accept='image/*'/><br>
        <img id='output'>
    </fieldset>
</template>
<script>
export default {
name: "UploadPhoto",
  props: {
    msg: String
  }
}
</script>
<style scoped>
legend {
    color:rgb(66, 6, 143);
    font-size: 25px;
}
img {
    width: 200px;
}
</style>