<template>
  <fieldset>
    <legend>{{msg}}</legend>
    <p>
      Телефон:
      <input
        type="tel"
        name="phone"
        pattern="[0-9]{3}-[0-9]{2}-[0-9]{2}"
        placeholder="111-11-11"
        v-model.lazy="valueInput.value1"
      >
    </p>
    <p>
      E-mail:
      <input type="email" placeholder="e-mail" v-model.lazy="valueInput.value2">
    </p>
    <p>
      Скайп:
      <input type="text" placeholder="skype" v-model.lazy="valueInput.value3">
    </p>
    <p>
      Телеграмм:
      <input type="text" placeholder="telegram" v-model.lazy="valueInput.value4">
    </p>
    <p>
      Сайт:
      <input type="url" placeholder="URL" v-model.lazy="valueInput.value5">
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
              value5: '',
            },
        }
    },
    name: 'ContactInformation',
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