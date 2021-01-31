<template>
  <h1 class="text-gray-200 text-3xl font-bold hover:text-white">
    {{ title }}
  </h1>
</template>

<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";

@Component
export default class Logo extends Vue {
  @Prop() title!: string;
}
</script>

<style>
</style>