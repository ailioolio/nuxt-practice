<template>
  <Overlay>
    <div class="modal">
      <CloseIcon class="modal__close" @close="close" />
      <slot />
    </div>
  </Overlay>
</template>

<script lang="ts">
import { defineComponent, SetupContext } from "@nuxtjs/composition-api";
import Overlay from "~/components/shared/Overlay.vue";
import CloseIcon from "~/components/shared/icons/CloseIcon.vue";

export default defineComponent({
  components: {
    Overlay,
    CloseIcon,
  },

  setup(_, context: SetupContext) {
    const close = () => {
      context.emit("close");
    };
    return {
      close,
    };
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

  &__close {
    position: absolute;
    top: 16px;
    right: 16px;
    // transition: 2s;
    cursor: pointer;
    &:hover {
      opacity: 0.5;
    }
  }

  // @media screen and (min-width: px) {
  // }
}
</style>
