<template>
  <fieldset>
    <legend>{{msg}}</legend>
    <p>
      Учреждение образования:
      <input type="text" placeholder="Ваше образование" v-model.lazy="valueInput.value1">
    </p>
    <p>
      Факультет:
      <input type="text" placeholder="Ваш факультет" v-model.lazy="valueInput.value2">
    </p>
    <p>
      Специализация:
      <input type="text" placeholder="Ваша специализация" v-model.lazy="valueInput.value3">
    </p>
    <p>
      Год завершения:
      <input type="month" name="monthYear" v-model.lazy="valueInput.value4">
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
              value1: '',
              value2: '',
              value3: '',
              value4: '',
            },
        }
    },
    name: 'Education',
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