<template>
  <Overlay>
    <div class="modal">
      <slot />
    </div>
  </Overlay>
</template>

<script lang="ts">
import { defineComponent } from "@nuxtjs/composition-api";
import Overlay from "~/components/shared/Overlay.vue";

export default defineComponent({
  components: {
    Overlay,
  },
});
</script>

<style lang="scss" scoped>
.modal {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 44px 16px;
  background-color: white;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border-radius: 16px;

  @media screen and (min-width: px) {
  }
}
</style>
