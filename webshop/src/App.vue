<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { ref } from 'vue'
import HeaderNav from './components/HeaderNav.vue'
import SpinningContent from './components/SpinningContent.vue'
</script>

<template>
  <HeaderNav />
  <SpinningContent />
  <RouterView />
</template>

<style scoped>

</style>
