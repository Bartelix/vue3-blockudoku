<template>
  <div class="brick">
    <div class="brick-element"></div>
    <div class="brick-element"></div>
    <div class="brick-element"></div>
  </div>
</template>

<script>
export default {
  name: "HorizontalPadleBrick",
};
</script>

<style scoped lang="scss">
$brick-element-size: clamp(3rem, 10vmin, 5rem);

.brick {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0.125rem;
  padding: 0.125rem;
  background-color: rgba(0, 0, 0, 0.7);
}

.brick-element {
  width: $brick-element-size;
  height: $brick-element-size;
  background-color: rgb(121, 182, 242);
}
</style>
