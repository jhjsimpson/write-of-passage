<template>
  <div id="input">
    <input
      id="commandLine"
      type="text"
      placeholder=">"
      onkeyup="this.value = this.value.toUpperCase();"
      autocomplete="off"
      spellcheck="false"
      maxlength="100"
    />
  </div>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";

export default class PassageGameInput extends Vue {
  msg!: string;
}
</script>
