<template>
  <div class="label">
    <span class="label__text">
      <slot />
    </span>
  </div>
</template>

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
</style>
