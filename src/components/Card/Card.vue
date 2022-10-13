<template>
  <div class="card">
    <div class="image"></div>
    <div class="info">
      <h2>
        {{ title }}
      </h2>
      <div class="buy">
        <div class="price">
          <h6 class="old">
            {{ oldPrice }}
          </h6>
          <h3>
            {{ price }}
          </h3>
        </div>
        <Button text="Купить"></Button>
      </div>
    </div>
  </div>
</template>

<script>
import Button from "components/Button/Button";
export default {
  name: "Card",
  components: {Button},
  props: {
    price: {
      type: String,
      required: true,
    },
    oldPrice: {
      type: String,
    },
    title: {
      type: String,
      required: true
    },
    link: {
      type: String,
      required: true,
    }
  }
}
</script>

<style scoped>
  @import "./Card.styles.scss";
</style>