<template>
    <div class="progress">
        <img src="./assets/formImg.jpg">
        <h2>{{msg}}</h2>
    </div>
</template>
<script>
export default {
name: "Progress",
  props: {
    msg: String
  }

}
</script>
<style scoped>
h2 {
    color:blueviolet;
}
img {
  width: 200px;
}
</style>

