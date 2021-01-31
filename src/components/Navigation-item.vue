<template>
  <h1 class="text-lg font-bold mx-8 text-gray-600 text-shadow-lg cursor-pointer hover:text-gray-800">{{ text }}</h1>
</template>

<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";

@Component
export default class NavigationItem extends Vue {
  @Prop() text!: string;
}
</script>

<style>
</style>