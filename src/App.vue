<template>
  <div id="app">
    <component :is="this.$route.meta.layout">
      <router-view />
    </component>
  </div>
</template>

<script>

export default {
  name: 'app',
  };
</script>

<style src="./assets/tailwind.css"></style>
