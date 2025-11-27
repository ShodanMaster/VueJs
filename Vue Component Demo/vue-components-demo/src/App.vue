<template>
    <h1>{{ message }}</h1>
    <p>This is a simple Vue.js application demonstrating component usage.</p>
    <ContactUs />
</template>

<script setup>
    import ContactUs from './components/ContactUs.vue';
    const message = "Hello from Vue 3!";
</script>
