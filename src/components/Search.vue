<template>
  <div class="px-4 py-3 xl:py-4 flex items-center rounded-full bg-gray-100 shadow-md">
    <img src="../assets/search.svg" alt="" class="w-4 h-4 mr-4" />
    <input
      class="text-sm text-gray-600 bg-transparent w-full focus:outline-none"
      placeholder="Search for a place, destinations..."
    />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Search extends Vue {}
</script>

<style>
</style>