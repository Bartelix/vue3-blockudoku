<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <GameBoard />
  <MoveBricks />
</template>

<script>
import GameBoard from "./components/GameBoard.vue";
import MoveBricks from "./components/MoveBricks.vue";

export default {
  name: "App",
  components: { GameBoard, MoveBricks },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
