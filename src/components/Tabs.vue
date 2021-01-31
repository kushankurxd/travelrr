<template>
  <div class="flex items-center overflow-auto">
    <span
      class="mr-6 xl:mr-12 font-medium text-gray-600 hover:text-gray-900 cursor-pointer text-shadow"
      v-bind:class="{ 'text-gray-900 underline font-semibold': selectedTab === index }"
      v-bind:key="tab.title"
      v-for="(tab, index) in tabs"
      @click="onTabSelected(index)"
      >{{ tab.title }}</span
    >
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop, Emit } from "vue-property-decorator";

@Component
export default class Logo extends Vue {
  @Prop() tabs!: Array<{ title: string; selected: boolean }>;
  selectedTab = 0;  

  @Emit('on-selected')
  onTabSelected (index: number): number {
      this.selectedTab = index;
      return index;
  }
}
</script>

<style>
</style>