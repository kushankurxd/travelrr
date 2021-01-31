<template>
  <div class="flex h-screen w-screen">
    <div class="h-full w-1/2 hidden sm:flex flex-col relative">
      <!-- Left image and its overlay -->
      <img
        src="../assets/travel-0.jpg"
        alt="image"
        class="absolute h-full w-full object-cover"
      />
      <div class="absolute inset-0 bg-gray-900 opacity-40 h-full"></div>

      <!-- Logo-text -->
      <Logo title="Travelrr" class="m-5 ml-8 z-10" />
      <div class="flex-1"></div>

      <div class="m-5 ml-8 mb-20 z-10">
        <h2 class="text-gray-200 text-4xl">Hey!</h2>
        <h2 class="text-white font-medium text-5xl mt-2">
          Where are you going on
        </h2>
        <h2 class="text-white font-medium text-5xl mt-2">
          Vaccation this Holidays?
        </h2>
        <!-- button -->
        <Button
          text="Plan a Vacation"
          class="mt-6 font-medium px-12 py-3 rounded-lg"
        />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Logo from "../components/Logo.vue";
import Button from "../components/Button.vue";

@Component({
  components: {
    Logo,
    Button,
  },
})
export default class Home extends Vue {}
</script>

<style scoped>
</style>