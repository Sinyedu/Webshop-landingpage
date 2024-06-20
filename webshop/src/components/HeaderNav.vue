<template>
    <header class="bg-white shadow-md">
        <div class="container mx-auto flex justify-between items-center p-4">
            <!-- Search Bar -->
            <div class="flex-1 mx-4">
                <input type="text" placeholder="Search..." class="w-full px-4 py-2 border rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
            </div>
            <!-- Hamburger Menu -->
            <div class="lg:hidden">
                <button @click="toggleMenu" class="text-gray-700 focus:outline-none focus:text-gray-900">
                    <svg class="h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
                    </svg>
                </button>
            </div>
            <!-- Navigation Links -->
            <nav class="hidden lg:flex items-center space-x-4">
                <router-link to="/" class="text-gray-700 hover:text-gray-900">Home</router-link>
                <router-link to="/products" class="text-gray-700 hover:text-gray-900">Products</router-link>
                <router-link to="/cart" class="text-gray-700 hover:text-gray-900">Cart</router-link>
            </nav>
        </div>
        <!-- Mobile Menu -->
        <div v-if="menuOpen" class="lg:hidden">
            <nav class="p-4 space-y-2">
                <router-link to="/" class="block text-gray-700 hover:text-gray-900">Home</router-link>
                <router-link to="/products" class="block text-gray-700 hover:text-gray-900">Products</router-link>
                <router-link to="/cart" class="block text-gray-700 hover:text-gray-900">Cart</router-link>
            </nav>
        </div>
    </header>
 </template>
 
 <script setup>
 import { ref } from 'vue';
 
 const menuOpen = ref(false);
 
 function toggleMenu() {
     menuOpen.value = !menuOpen.value;
 }
 </script>
 
 <style scoped>
 .container {
     max-width: 1200px;
 }
 </style>
 