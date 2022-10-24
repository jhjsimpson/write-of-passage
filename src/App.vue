<!-- eslint-disable prettier/prettier -->
<template>
  <PassageGame msg="# PRESS ANY KEY" />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import PassageGame from "./components/PassageGame.vue";
import "@fontsource/press-start-2p";

@Options({
  components: {
    PassageGame,
  },
})
export default class App extends Vue {}
</script>

<style>
body {
  margin-top: 100px;
  background-color: black;
}
h1 {
  font-family: "Press Start 2P", monospace;
  font-size: 22px;
  text-align: center;
  color: #4cc005;
  background-color: black;
}
table {
  width: 80%;
  margin: 0 auto;
  border-style: solid;
  border-color: #4cc005;
  padding: 20px;
}
</style>
