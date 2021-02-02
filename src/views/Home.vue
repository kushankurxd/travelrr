<template>
  <div class="flex h-screen w-screen">
    <div class="h-full w-1/2 hidden lg:flex flex-col relative">
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
        <h2 class="text-gray-200 text-3xl xl:text-4xl">Hey!</h2>
        <h2 class="text-white font-medium text-4xl xl:text-5xl mt-2">
          Where are you going on
        </h2>
        <h2 class="text-white font-medium text-4xl xl:text-5xl mt-2">
          Vaccation this Holidays?
        </h2>
        <!-- button -->
        <Button
          text="Plan a Vacation"
          class="mt-6 font-medium px-12 py-3 rounded-lg"
        />
      </div>
    </div>

    <!-- Right section -->
    <div class="h-full w-full lg:w-1/2 flex flex-col relative">
      <!-- Navigation menu -->
      <div class="flex flex-row items-center m-5">
        <Hamburger />
        <div class="flex-1 flex justify-end items-center">
          <NavigationItem text="Travelrr Stories" class="hidden sm:block" />
          <NavigationItem text="Blog" class="hidden sm:block" />
          <ProfileAvatar class="ml-10" />
        </div>
      </div>

      <!-- Heading  -->
      <div class="m-5">
        <h2
          class="font-bold text-4xl xl:text-5xl xxl:text-xl text-shadow-md text-gray-900"
        >
          Let's Enjoy
        </h2>
        <h2
          class="font-bold text-4xl xl:text-5xl xxl:text-xl mt-2 text-shadow-md text-gray-900"
        >
          the Vacations!
        </h2>
      </div>

      <!-- Search -->
      <div class="m-5 mr-5 lg:mr-8 md:mr-20 xl:mr-20">
        <Search />
      </div>

      <!-- tabs -->
      <div class="m-5">
        <Tabs v-bind:tabs="tabs" @on-selected="onTabSelected" />
      </div>

      <div class="m-5 overflow-auto grid xl:grid-cols-3 xl:gap-4">
        <TravelCard image="eiffel-tower.jpg" title="Eiffel Tower" subtitle="Paris" opacity="opacity-10" />
        <TravelCard image="giant-bomb.jpg" title="Giant Bomb" subtitle="Dubai" opacity="opacity-40" />
        <TravelCard image="fly-night.jpg" title="Eiffel Tower" subtitle="Singapore" opacity="opacity-20" />  
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Logo from "../components/Logo.vue";
import Button from "../components/Button.vue";
import Hamburger from "../components/Hamburger.vue";
import NavigationItem from "../components/Navigation-item.vue";
import ProfileAvatar from "../components/Profile-avatar.vue";
import Search from "../components/Search.vue";
import Tabs from "../components/Tabs.vue";
import TravelCard from "../components/Travel-Card.vue";

@Component({
  components: {
    Logo,
    Button,
    Hamburger,
    NavigationItem,
    ProfileAvatar,
    Search,
    Tabs,
    TravelCard,
  },
})
export default class Home extends Vue {
  tabs = [
    {
      title: "All",
    },
    {
      title: "New",
    },
    {
      title: "Reccomended",
    },
    {
      title: "Most Visited",
    },
  ];

  onTabSelected(index: number): void {
    console.log(index);
  }
}
</script>

<style scoped>
</style>