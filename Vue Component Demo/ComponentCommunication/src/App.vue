
<template>
  <h1>{{ message }}</h1>
  <input type="text" v-model="owner">
  <ContactUs name="John Doe" :phone="9876543120" :owner="owner"></ContactUs>
  <ContactUs name="Jane Doe" :phone="1234567890" :owner="owner" email="jane@example.com"></ContactUs>

  <div class="row">
    <div class="col-12" v-for="contact in contacts" :key="contact.id">
      <Contact 
        :name="contact.name"
        :phone="contact.phone"
        :owner="contact.ownerName"
        :isFav="contact.isFav"
      ></Contact>
    </div>
  </div>

</template>

<script setup>
import { ref, reactive } from 'vue';
import ContactUs from './components/ContactUs.vue'
import Contact from './components/Contact.vue'
const message = "Hello World!";
const owner = ref("Shodan");

const contacts = reactive([
  {
    id: 1,
    name: "Akshay",
    phone: 9876543210,
    ownerName: owner,
    isFav: false,
  },
  {
    id: 2,
    name: "Shodan",
    phone: 9876543211,
    ownerName: owner,
    isFav: true,
  },
  {
    id: 3,
    name: "Kannan",
    phone: 9876543212,
    ownerName: owner,
    isFav: false,
  },
])

</script>
<style scoped></style>
