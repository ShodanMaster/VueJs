<template>
    <div class="row">
        <div class="col-12" v-for="contact in contacts" :key="contact.id">
            <Contact 
                :name="contact.name"
                :phone="contact.phone"
                :email="contact.email"
                :isFav="contact.isFav"
                :message="contact.message"
                @updateFav="onUpdateEvent(contact, $event)"
            />
        </div>
    </div>
</template>

<script setup>
import { reactive } from 'vue'
import Contact from './components/Contact.vue'

const contacts = reactive([
    {
        id: 1,
        name: "Akshay",
        phone: 9876543210,
        email: "akshay@example.com",
        isFav: false,
        message: "",
    },
    {
        id: 2,
        name: "Shodan",
        phone: 98765432101,
        isFav: true,
        message: "",
    },
    {
        id: 3,
        name: "Kannan",
        phone: 9876543210,
        email: "kannan@example.com",
        isFav: false,
        message: "",
    },
])

function onUpdateEvent(contact, message) {
    contact.isFav = !contact.isFav
    contact.message = contact.isFav ? message : ""
}
</script>
