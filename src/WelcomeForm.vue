<script setup>
import { ref } from "vue";

const name = ref("");
const age = ref("");
const address = ref("");
const course = ref("");
const year = ref("");

const props = defineProps({
  course: String,
  year: String

});

</script>

<template>
  <h2>Welcome Form</h2>

  <input v-model="name" type="text" placeholder="Name" required />
  <input v-model="age" type="number" placeholder="Age" required />
  <input v-model="address" type="text" placeholder="Address" required />

  <p>Course: {{ props.course }}</p>
  <p>Year: {{ props.year }}</p>

  <h3>Welcome, {{ name }}!</h3>

  <p>Age: {{ age }}</p>
  <p>Address: {{ address }}</p>
</template>