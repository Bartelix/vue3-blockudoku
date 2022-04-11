<template>
  <div class="brick-element"></div>
</template>

<script>
export default {
  name: "BaseBrick",
};
</script>

<style scope lang="scss">
$brick-element-size: clamp(3rem, 10vmin, 5rem);

.brick-element {
  width: $brick-element-size;
  height: $brick-element-size;
  background-color: rgb(121, 182, 242);
  border: 1px solid #fff;
}
</style>
