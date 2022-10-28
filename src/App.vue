<!-- eslint-disable prettier/prettier -->
<template>
  <PassageGame msg="TEST"/>
  <PassageGameFooter />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import PassageGame from "./components/PassageGame.vue";
import PassageGameFooter from "./components/PassageGameFooter.vue";
import "@fontsource/press-start-2p";

@Options({
  components: {
    PassageGame,
    PassageGameFooter,
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
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: repeating-linear-gradient(
    0deg,
    rgba(255, 255, 255, 0),
    rgba(0, 0, 0, 0.25) 2px,
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
#main {
  position: fixed;
  width: 100vw;
  height: 90vh;
  padding: 2rem;
}
#footer {
  position: fixed;
  width: 100vw;
  height: 10vh;
  bottom: 0;
  padding: 2rem;
}
h1,
h2,
h3 {
  margin: 0;
}
</style>
