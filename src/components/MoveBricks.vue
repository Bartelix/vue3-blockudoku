<template>
  <div class="move-bricks-wrapper">
    <div class="move-brick-wrapper" v-for="i in 3" :key="i">
      <component :is="bricks[i - 1]" />
    </div>
  </div>
</template>

<script>
import BaseBrick from "./BaseBrick.vue";
import HorizontalPadleBrick from "./HorizontalPadleBrick.vue";

export default {
  name: "MoveBricks",
  components: {
    BaseBrick,
    HorizontalPadleBrick,
  },
  computed: {
    bricks() {
      return ["BaseBrick", "BaseBrick", "HorizontalPadleBrick"];
    },
  },
};
</script>

<style scoped>
.move-bricks-wrapper {
  display: flex;
  justify-content: space-evenly;
  padding: 5rem 10rem;
}
</style>
