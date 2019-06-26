<template>
    <fieldset>
        <legend>{{msg}}</legend>
        <p>Учреждение образования: <input type="text" placeholder="Ваше образование"/></p>
        <p>Факультет: <input type="text" placeholder="Ваш факультет"/></p>
        <p>Специализация: <input type="text" placeholder="Ваша специализация"/></p>
        <p>Год завершения: <input type="month" name="monthYear"/></p>
    </fieldset>
</template>
<script>
export default {
name: "Education",
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