<template>
  <div class="main">
    <h1 class="main__hello">{{ hello }}</h1>
    <CategoryLabel>場所</CategoryLabel>
    <div class="main__user">
      <UserIcon
        imagePath="https://ca.slack-edge.com/THKEQG3CG-U01U57LGAJ0-01665b4814b7-512"
        imageAlt="あーりおおーりおぺぺろんちーの"
      />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "@nuxtjs/composition-api";
import CategoryLabel from "~/components/shared/CategoryLabel.vue";
import UserIcon from "~/components/shared/UserIcon.vue";

export default defineComponent({
  components: {
    CategoryLabel,
    UserIcon,
  },
  setup() {
    const hello = ref<string>("Hello, world!");

    return {
      hello,
    };
  },
});
</script>

<style lang="scss" scoped>
.main {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;

  &__hello {
    font-size: 28px;
  }

  &__user {
    width: 60px;
    height: 60px;
  }
}
</style>
