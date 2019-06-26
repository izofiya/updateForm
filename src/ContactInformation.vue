<template>
    <fieldset>
        <legend>{{msg}}</legend>
        <p>Телефон: <input type="tel" name="phone" pattern="[0-9]{3}-[0-9]{2}-[0-9]{2}" placeholder="111-11-11"/>
        <p>E-mail: <input type="email" placeholder="e-mail" /></p>
        <p>Скайп: <input type="text" placeholder="skype" /></p>
        <p>Телеграмм: <input type="text" placeholder="telegram" /></p>
        <p>Сайт: <input type="url" placeholder="URL" /></p>
    </fieldset>
</template>
<script>
export default {
name: "ContactInformation",
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
p {
    color:rgb(4, 3, 70);
    font-size: 20px;
}
</style>