<template>

  <!-- Contact Us Section -->
  <v-container id="contact-us" class="my-5">
      <v-form @submit.prevent="submitForm">
        <v-text-field v-model="form.name" label="Nombre" required></v-text-field>
        <v-text-field v-model="form.neighborhood" label="Colonia Solicitante" required></v-text-field>
        <v-text-field v-model="form.phone" label="Número de Contacto" required></v-text-field>
        <v-textarea v-model="form.message" label="Mensaje Adicional" required></v-textarea>
        <v-btn type="submit" color="#ff4254">Enviar</v-btn>
      </v-form>
    </v-container>
</template>
<script setup>
import { ref } from 'vue';

const form= ref({
        name: '',
        neighborhood: '',
        phone: '',
        message: '',
      });
</script>
