<template>
  <fieldset>
    <legend>{{msg}}</legend>
    <p>
      Имя:
      <input name="inpName" id="nameForm" type="text" placeholder="Ваше имя" v-model.lazy="valueInput.name">
    </p>
    <p>
      Фамилия:
      <input id="name2Form" type="text" placeholder="Ваша фамилия" v-model.lazy="valueInput.name2">
    </p>
    <p>
      Отчество:
      <input id="name3Form" type="text" placeholder="Ваше отчество" v-model.lazy="valueInput.name3">
    </p>
    <p>
      Дата рождения:
      <input id="dateForm" type="date" name="date" v-model.lazy="valueInput.date">
    </p>
      <ul>
          <li v-for="value in valueInput">{{ value }}</li>
      </ul>
  </fieldset>
</template>
<script>
export default {
   data() {
        return {
            valueInput: {
              name: '',
              name2: '',
              name3: '',
              date: '',
            },
        }
    },
    name: 'TotalInformation',
    props: {
        msg: String,
    },
}
</script>
<style scoped>
legend {
    color: rgb(66, 6, 143);
    font-size: 25px;
}
p {
    color: rgb(4, 3, 70);
    font-size: 20px;
}
</style>