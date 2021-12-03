<template>
  <div class="label" :class="{ large: isLarge }">
    <span class="label__text">
      <slot />
    </span>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from "@nuxtjs/composition-api";

export default defineComponent({
  props: {
    isLarge: {
      type: Boolean as PropType<boolean>,
      default: false,
    },
  },
  setup() {},
});
</script>

<style lang="scss" scoped>
.label {
  width: 60px;
  height: 28px;
  border-radius: 14px;
  background-color: #4eb2d6;
  text-align: center;

  &__text {
    color: white;
    font-size: 14px;
    font-weight: bold;
    line-height: 28px;
  }
}

.large {
  width: 88px;
}
</style>
