<template>
  <div class="bg-gray-200 h-64 xl:h-72 rounded-xl relative">
    <img
      :src="require(`../assets/${image}`)"
      class="rounded-xl h-64 xl:h-72 w-full object-cover absolute z-auto"
    />
    <!-- Overlay -->
    <div
      class="absolute inset-0 bg-gray-900 opacity-0 h-full rounded-xl"
      v-bind:class="`${opacity}`"
    ></div>

    <div class="absolute z-auto bottom-0 m-4 flex flex-row items-center">
      <img src="../assets/map-pin.svg" class="w-4 h-4" alt="" />
      <div class="ml-2">
        <p class="text-white font-medium">{{ title }}</p>
        <p class="text-xs text-gray-200">{{ subtitle }}</p>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class TravelCard extends Vue {
  @Prop() image!: string;
  @Prop() title!: string;
  @Prop() subtitle!: string;

  // more-custom
  @Prop() opacity!: string;
}
</script>

<style>
</style>