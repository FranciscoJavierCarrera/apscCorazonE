<template>
  <v-app>
    <!-- Hero Section -->
    <v-container id="hero" fluid class="pa-0">
      <v-carousel cycle height="70vh">
        <v-carousel-item v-for="(image, i) in images" :key="i">
          <v-img :src="image" height="100%" width="100%" cover></v-img>
        </v-carousel-item>
      </v-carousel>
    </v-container>

    <!-- About Us Section -->
    <v-container id="about-us" class="my-5">
      <v-row>
        <v-col cols="12" md="4" v-for="(item, index) in aboutItems" :key="index">
          <v-card>
            <v-card-title>{{ item.title }}</v-card-title>
            <v-card-text>{{ item.text }}</v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>

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
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      images: [
        'public/img/eworu7qowigjehr581y314b.jpg',
        'public/img/dsfiua9s8y3qwrni7t0127519i3wjnfkjshf9.jpg',
        'public/img/134p8uerwkgh2354987134ndfivbu247hpg.jpg',
        'public/img/health-4385852_1280.jpg',
        'public/img/veterinarian-4906607_1280.jpg',
      ],
      aboutItems: [
        { title: 'Misión', text: 'Proteger y cuidar a los animales de compañía en nuestra comunidad.' },
        { title: 'Visión', text: 'Un mundo donde todos los animales sean tratados con respeto y amor.' },
        { title: 'Valores', text: 'Compasión, Responsabilidad, Respeto y Solidaridad.' },
      ],
      form: {
        name: '',
        neighborhood: '',
        phone: '',
        message: '',
      }
    };
  },
  methods: {
    submitForm() {
      console.log('Formulario enviado:', this.form);
    },
  },
};
</script>

<style>
/* Puedes agregar estilos personalizados aquí si es necesario */
</style>
