<template>
  <div class="overlay">
    <slot />
  </div>
</template>

<style lang="scss" scoped>
.overlay {
  width: 100%;
  height: 100%;
  position: fixed;
  top: 0;
  left: 0;
  background-color: black;
  opacity: 0.5;
}
</style>
