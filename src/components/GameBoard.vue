<template>
  <div class="game-board">
    <div class="game-board-cells">
      <div v-for="i in size * size" :key="i" :class="cellClasses(i)"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "GameBoard",
  components: {},
  data() {
    return {
      size: 9,
    };
  },
  methods: {
    cellClasses(i) {
      const r = Math.floor((i - 1) / this.size);
      const c = (i - 1) % this.size;

      const isGray =
        ((r <= 2 || r >= 6) && (c <= 2 || c >= 6)) ||
        (r >= 3 && r <= 5 && c >= 3 && c <= 5);

      return `cell cell--${isGray ? "gray" : "white"}`;
    },
  },
};
</script>

<style scoped lang="scss">
$cell-size: clamp(3rem, 10vmin, 5rem);

.game-board {
  display: flex;
  justify-content: center;
}
.game-board-cells {
  display: grid;
  grid-template-columns: repeat(9, 1fr);
  gap: 0.125rem;
  padding: 0.125rem;
  background-color: rgba(0, 0, 0, 0.7);
}
.cell {
  width: $cell-size;
  height: $cell-size;

  &.cell--white {
    background-color: #fff;
  }

  &.cell--gray {
    background-color: #ddd;
  }
}
</style>
