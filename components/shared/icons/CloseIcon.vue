<template>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    width="17.671"
    height="17.671"
    viewBox="0 0 17.671 17.671"
    @click="close"
  >
    <g
      id="グループ_4099"
      data-name="グループ 4099"
      transform="translate(-691.672 -78.672)"
    >
      <line
        id="線_33"
        data-name="線 33"
        x2="12.014"
        y2="12.014"
        transform="translate(694.5 81.5)"
        fill="none"
        stroke="#b5b5b5"
        stroke-linecap="round"
        stroke-width="4"
      />
      <line
        id="線_34"
        data-name="線 34"
        y1="12.014"
        x2="12.014"
        transform="translate(694.5 81.5)"
        fill="none"
        stroke="#b5b5b5"
        stroke-linecap="round"
        stroke-width="4"
      />
    </g>
  </svg>
</template>

<script lang="ts">
import { defineComponent, SetupContext } from "@nuxtjs/composition-api";

export default defineComponent({
  setup(_, context: SetupContext) {
    const close = () => {
      context.emit("close");
    };

    return { close };
  },
});
</script>
