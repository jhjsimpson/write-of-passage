<template>
  <div id="main">
    <table>
      <tr>
        <h1>{{ msg }}</h1>
      </tr>
    </table>
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
