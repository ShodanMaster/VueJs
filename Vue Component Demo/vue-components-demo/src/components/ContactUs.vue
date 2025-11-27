<template>
    <div class="">
        <h1>Contact Us!</h1>
        <p>Please reach out to us at {{ email }}.</p>
        <ButtonCounter />
        <ButtonCounter />
    </div>
</template>
<script setup>
    import ButtonCounter from '../ButtonCounter.vue';
    const email = "contact@example1.com";
</script>