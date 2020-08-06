<template>
  <div class="flex items-center rounded-lg bg-white shadow-lg overflow-hidden">
    <img class="h-32 w-35 flex-shrink-0" :src="destination.imageUrl" :alt="destination.imageAlt">
    <div class="px-6 py-4">
      <h3 class="text-lg font-semibold text-gray-800">{{ destination.name }}</h3>
      <p class="text-gray-600">{{ destination.description }}</p>
      <div class="mt-4">
        <a href="#" class="text-indigo-500 hover:text-indigo-400 font-semibold text-sm">Explore {{ destination.name }}</a>
      </div>
    </div>
  </div>
</template> 
 
<script>
export default {
  props: ['destination'],
}
</script>

