<template>
  <div class="cursor-pointer">
    <div class="bars"></div>
    <div class="bars long"></div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Hamburger extends Vue {}
</script>

<style scoped>
.bars {
  background-color: #000000;
  height: 3px;
  width: 24px;
  margin-top: 5px;
  border-radius: 4px;
}

.long {
  width: 30px;
}
</style>