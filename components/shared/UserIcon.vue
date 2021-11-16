<template>
  <img :src="imagePath" :alt="imageAlt" class="icon" />
</template>

<script lang="ts">
import { defineComponent, PropType } from "@nuxtjs/composition-api";

export default defineComponent({
  props: {
    imagePath: {
      type: String as PropType<string>,
      required: true,
    },
    imageAlt: {
      type: String as PropType<string>,
      // required: true,
      default: "userIcon",
    },
  },
});
</script>

<style lang="scss" scoped>
.icon {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  border: solid 2px #4eb2d6;
}
</style>
