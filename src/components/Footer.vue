<template>
<!-- Footer -->
<v-footer color="#f78c49" dark>
      <v-container>
        <v-row justify="center">
          <v-btn v-for="(social, index) in socials" :key="index" :href="social.link" target="_blank" icon>
            <v-icon>{{ social.icon }}</v-icon>
          </v-btn>
        </v-row>
      </v-container>
    </v-footer>
</template>

<script setup>
import { ref } from 'vue';


  const socials = ref([
    { icon: 'mdi-facebook', link: 'https://www.facebook.com/asociacion.protectora.de.mascotas.corazo' },
    { icon: 'mdi-twitter', link: 'https://twitter.com' },
    { icon: 'mdi-instagram', link: 'https://instagram.com' },
  ]);

</script>

<style scoped lang="sass">
  .social-link :deep(.v-icon)
    color: rgba(var(--v-theme-on-background), var(--v-disabled-opacity))
    text-decoration: none
    transition: .2s ease-in-out

    &:hover
      color: rgba(25, 118, 210, 1)
</style>
