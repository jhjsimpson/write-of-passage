<template>
  <div id="input">
    <!-- <h2 id="playerInput">> THIS IS SOME TEXT</h2> -->
    <div id="inputBox">
      <input id="playerInput" type="text" placeholder="Text" />
    </div>
  </div>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";

export default class PassageGameInput extends Vue {
  msg!: string;
}
</script>
