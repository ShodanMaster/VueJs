<template>
    <div class="rounded p-4 m-2" :class="isFav ? 'bg-info' : 'bg-warning'">
        <h3>Name: {{ name }}</h3>
        <p>Phone: {{ phone }}</p>
        <p class="float-end small" v-if="owner !=''">
            *Contact owner: {{ owner }}
        </p>
    </div>
</template>
<script setup>
const props = defineProps({
    name: {type: String, required: true},
    phone: Number,
    owner: String,
    isFav: {type:Boolean, default: false},
});

</script>