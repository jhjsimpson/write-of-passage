<!-- eslint-disable prettier/prettier -->
<template>
  <PassageGame msg="&> PRESS ANY KEY" />
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
  height: 100vh;
  margin: 0;
  overflow: hidden;
  padding: 2rem;
  color: rgb(15, 230, 15);
  font: 10px "Press Start 2p", monospace;
  text-shadow: 0 0 5px #182e15;
  pointer-events: none;
}

body::after {
  content: "";
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
  position: relative;
  height: 100vh;
}
#footer {
  position: absolute;
  bottom: 50px;
}
</style>
