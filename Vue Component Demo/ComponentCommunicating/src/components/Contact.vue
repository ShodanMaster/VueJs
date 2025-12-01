<template>
    <div class="rounded p-2 mb-3" :class="isFav ? 'bg-info' : 'bg-warning'">
        <p>Name: {{ name }}</p>
        <p>Phone: {{ phone }}</p>
        <p>Email: {{ email }}</p>

        <button class="btn" :class="[isFav ? 'btn-warning' : 'btn-success']" @click="toggleFav">
            {{ isFav ? 'Remove' : 'Add' }}
        </button>
        <div 
            class="bg-danger text-white rounded m-1 p-1" 
            id="message" 
            v-if="isFav && message"
        >
            {{ message }}
        </div>

    </div>
</template>
<script setup>

const props = defineProps({
    name: {type: String, required: true},
    phone: Number,
    email: {type: String, required: false, default: 'nil'},
    isFav: {type: Boolean, default: false},
    message: String,
});

const emit = defineEmits(["updateFav"]);

function toggleFav(){
    console.log('clicked');
    emit("updateFav", "This is your Favourite Contact");
}
</script>