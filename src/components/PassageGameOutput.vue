<template>
  <div id="output">
    <h2>{{ msg }}</h2>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  props: {
    msg: String,
  },
})
export default class PassageGameOutput extends Vue {
  msg!: string;
}
</script>
