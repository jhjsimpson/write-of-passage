<!-- eslint-disable prettier/prettier -->
<template>
  <PassageGameOutput msg="THIS IS SOME TEXT TEXT TO FILL THE DIV BASED 
  ON SCREEN SIZE OR SOMETHING. PLEASE KEEP TYPING FOR YOUR CONVENIENCE."/>
  <PassageGameInput />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import PassageGameOutput from "./components/PassageGameOutput.vue";
import PassageGameInput from "./components/PassageGameInput.vue";
import "@fontsource/press-start-2p";

@Options({
  components: {
    PassageGameOutput,
    PassageGameInput,
  },
})
export default class App extends Vue {}
</script>

<style>
body {
  background-color: black;
  background-image: radial-gradient(rgba(0, 150, 0, 0.75), black 120%);
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  color: rgb(15, 230, 15);
  font: 10px "Press Start 2p", monospace;
  text-shadow: 0 0 5px #182e15;
  pointer-events: none;
  margin: 0;
}

body::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: repeating-linear-gradient(
    0deg,
    rgba(255, 255, 255, 0),
    rgba(0, 0, 0, 0.75) 2px,
    transparent 1px,
    transparent 2px
  );
}

::selection {
  background: rgba(0, 0, 0, 0.373);
  text-shadow: none;
}
#app {
  position: fixed;
  height: 100vh;
  width: 100vw;
  display: inline-block;
}
#output {
  position: fixed;
  width: 100vw;
  height: 95vh;
  padding: 2rem;
}
#input {
  position: absolute;
  width: 100vw;
  height: 5vh;
  bottom: 0;
  margin: auto;
  padding: 2rem;
}
h1,
h2 {
  margin: 0;
}
#inputBox {
  position: absolute;
  bottom: 0;
  left: 0;
  margin: auto;
  padding: 2rem;
  background-color: rgba(0, 0, 0, 0);
  z-index: 1;
  color: rgb(15, 230, 15);
}
#playerInput {
  border: 0;
  background-color: rgba(0, 0, 0, 0);
  font: 2em "Press Start 2p", monospace;
}
</style>
