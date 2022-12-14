<template>
  <div id="output">
    <p>{{ msg }}</p>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  props: {
    msg: String,
  },
  data() {
    let commandList = "";
  },
})
export default class PassageGameOutput extends Vue {
  msg!: string;
}
</script>
