<template>
  <div class="move-bricks-wrapper">
    <div class="move-brick-wrapper" v-for="i in 3" :key="i">
      <BaseBrick />
    </div>
  </div>
</template>

<script>
import BaseBrick from "./BaseBrick.vue";

export default {
  name: "MoveBricks",
  components: {
    BaseBrick,
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
