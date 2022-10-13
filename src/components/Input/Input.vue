<template>
  <div class="wrapper">
    <input class="input" placeholder="Поиск по названию картины"/>
    <Button text="Найти"></Button>
  </div>
</template>

<script>
import Button from "components/Button/Button";
export default {
  name: "Input",
  components: {Button}
}
</script>

<style scoped>
  @import "./Input.styles.scss";
</style>