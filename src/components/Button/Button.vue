<template>
  <button class="button" :class="{
    'button--loading': isLoading,
    'button--withIcon': isInBucket
  }">
    <Loading v-if="isLoading" class="loading__icon"/>
    <Vector v-if="isInBucket"/>
    {{ text }}
  </button>
</template>

<script>
import Tick from "components/icons/Tick";
import Loading from "components/icons/Loading";

export default {
  name: "Button",
  props: {
    text: {
      type: String,
      required: true,
    },
    isLoading: {
      type: Boolean,
    },
    isInBucket: {
      type: Boolean,
    }
  },
  components: {
    Tick, Loading
  }
}
</script>

<style scoped>
  @import "./Button.styles.scss";
</style>