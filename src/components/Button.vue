<template>
  <button
    class="button px-4 py-2 bg-gray-100 hover:bg-gray-200 text-black w-max rounded focus:outline-none shadow-lg hover:shadow-xl"
  >
    {{ text }}
  </button>
</template>

<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";

@Component
export default class Button extends Vue {
  @Prop() text!: string;
}
</script>

<style>
</style>