<template>
  <div id="app">
    <div class="bg-taupe flex">
      <div class="px-5 py-15 max-w-md mx-auto sm:max-w-xl lg:max-w-full lg:w-1/2 lg:py-24 lg:px-12">
        <div class="xl:max-w-lg xl:ml-auto">
          <img class="h-35 w-35 lg:hidden" src="/img/default.svg" alt="Full Serve">
          <img class="mt-6 rounded-lg shadow-xl sm:mt-8 sm:h-64 sm:w-full sm:object-cover sm:object-center lg:hidden" src="/img/coworking-hero.jpeg" alt="Bright and airy coworking space">
          <h1 class="mt-3 text-2xl font-bold text-gray-900 leading-tight sm:mt-2 sm:text-4xl lg:text-3xl xl:text-4xl">
           Full Serve is your new coworking paradise.
            <br class="hidden lg:inline"><span class="text-indigo-500">Take advantage of it.</span>
          </h1>
          <p class="mt-2 text-gray-600 sm:mt-4 sm:text-xl">
            Full Serve let's you escape your normal surroundings. Featuring themed, work-friendly spaces and spa-like amenities for feeling like you're on vacation, even when you're working.
          </p>
          <div class="mt-4 sm:mt-6 mb-4">
            <a href="#" class="btn btn-indigo shadow-lg sm:text-base">Plan your escape</a>
          </div>
        </div>
      </div>
      <div class="hidden lg:block lg:w-1/2 lg:relative">
        <img class="absolute inset-0 h-full w-full object-cover object-center" src="/img/coworking-hero.jpeg" alt="Bright and airy coworking space
        ">
      </div>
    </div>
    <div class="sm:bg-taupe md:bg-taupe-lighter">
      <div class="max-w-md sm:max-w-xl lg:max-w-6xl mx-auto px-8 lg:px-12 py-8">
        <h2 class="text-xl text-gray-900">Popular packages</h2>
        <p class="text-gray-600">Curated spaces, set up mindfully for your success.</p>
        <div class="flex flex-wrap -mx-10">
          <div class="mt-6 h-full w-full px-4 lg:w-1/2" v-bind:key="destination" v-for="destination in popularDestinations">
            <DestinationCard :destination="destination"/>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import DestinationCard from './components/DestinationCard'

export default {
  name: 'app',
  components: {
    DestinationCard,
  },
  data() {
    return {
      popularDestinations: [
        {
          name: 'Portland',
          description: 'Perfect for small groups',
          imageUrl: '/img/portland.jpeg',
          imageAlt: 'Small Meeting Space',
        },
        {
          name: 'Brooklyn',
          description: 'Perfect for medium groups',
          imageUrl: '/img/present.jpeg',
          imageAlt: 'Presentation Room',
        },
        {
          name: 'Newport',
          description: 'Perfect for one-on-one meetings',
          imageUrl: '/img/meet-me.jpeg',
          imageAlt: 'Beach in Miami',
        },
        {
          name: 'Seattle',
          description: 'Explore the communal kitchen',
          imageUrl: '/img/park-city.jpeg',
          imageAlt: 'The Kitchen',
        },
      ]
    }
  }
}
</script>

<style src="./assets/tailwind.css"></style>
