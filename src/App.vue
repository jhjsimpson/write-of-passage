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
* {
  box-sizing: border-box;
  pointer-events: all;
  margin: 0;
}

body {
  background-color: black;
  background-image: radial-gradient(rgba(0, 150, 12, 0.5), black 200%);
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  color: rgb(15, 230, 15);
  font: 1rem "Press Start 2p", monospace;
  text-shadow: 0 0 5px #182e15;
  padding: 0;
  line-height: 1.2;
  pointer-events: none;
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
    rgba(0, 0, 0, 0.5) 2px,
    transparent 1px,
    transparent 2px
  );
  pointer-events: none;
}

::selection {
  background: rgba(0, 0, 0, 0.373);
  text-shadow: none;
}
#app {
  position: fixed;
  height: 100vh;
  width: 100vw;
  padding: 0;
}
#output {
  position: fixed;
  width: 100vw;
  height: 90vh;
  top: 0;
  margin: auto;
  padding: 2rem;
}
#input {
  position: fixed;
  width: 100vw;
  height: 10vh;
  bottom: 0;
  margin: auto;
}

#commandLine {
  position: absolute;
  bottom: 2rem;
  width: 100vw;
  border: 0;
  background-color: rgba(0, 0, 0, 0);
  font: 1rem "Press Start 2p", monospace;
  outline: none;
  color: rgb(15, 230, 15);
  padding: 0 2rem;
}

::placeholder {
  color: rgb(15, 230, 15);
  opacity: 1;
  outline: none;
}
</style>
