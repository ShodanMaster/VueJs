
<template>
  <h1>{{ message }}</h1>
  <ContactUs name="John Doe" phone="9876543120"></ContactUs>

</template>

<script setup>
import ContactUs from './components/ContactUs.vue'
const message = "Hello World!";

</script>
<style scoped></style>
