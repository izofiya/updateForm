<template>
    <fieldset>
        <legend>{{msg}}</legend>
        <p>Имя: <input name="inpName" id="nameForm" type="text" placeholder="Ваше имя" v-model="message" @keyup.enter="saveMessage"/></p>
        <p>Фамилия: <input id="name2Form" type="text" placeholder="Ваша фамилия" /></p>
        <p>Отчество: <input id="name3Form" type="text" placeholder="Ваше отчество" /></p>
        <p>Дата рождения: <input id="dateForm" type="date" name="date"/></p>
    </fieldset>
</template>
<script>
export default {
name: "TotalInformation",
  props: {
    msg: String
  },
  data() {
    return {
      message: ''
    }
  },
  methods: {
    saveMessage: function() {
      this.$emit('message', this.message);
    }
  }
}
</script>
<style scoped>
legend {
    color:rgb(66, 6, 143);
    font-size: 25px;
}
p {
    color:rgb(4, 3, 70);
    font-size: 20px;
}
</style>