<template>
  <v-app>
    <AppHeader />
    <v-main>
      <AppHome />
    </v-main>
    <Footer />
  </v-app>
</template>

<script setup>
import AppHeader from './components/Header.vue';
import AppHome from './components/AppHome.vue';
import Footer from './components/Footer.vue';
</script>
