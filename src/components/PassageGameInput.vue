<template>
  <div id="input">
    <input
      id="commandLine"
      type="text"
      placeholder=""
      onkeyup="this.value = this.value.toUpperCase();"
      autocomplete="off"
      spellcheck="false"
      maxlength="100"
      ref="cmdLine"
      v-on:keypress.enter="submitCommandLine"
    />
  </div>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";

export default class PassageGameInput extends Vue {
  mounted() {
    this.$refs.cmdLine.focus();
  }
}
</script>
