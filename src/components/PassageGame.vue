<template>
  <div id="main">
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
export default class PassageGame extends Vue {
  msg!: string;
}
</script>
