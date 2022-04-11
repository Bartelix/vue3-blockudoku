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

<style scope lang="scss">
$brick-element-size: clamp(3rem, 10vmin, 5rem);

.brick {
  display: flex;
}

.brick-element {
  width: $brick-element-size;
  height: $brick-element-size;
  background-color: rgb(121, 182, 242);
  border: 1px solid #fff;
}
</style>
