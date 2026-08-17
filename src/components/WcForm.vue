<script setup>
import { ref } from "vue";

const props = defineProps({
  name: String,
  age: Number,
  address: String,
  course: String,
  year: String
});

const name = ref(props.name);
const age = ref(props.age);
const address = ref(props.address);
const course = ref(props.course);
const year = ref(props.year);
</script>

<template>
  <h2>Welcome Form</h2>

  <input
    v-model="name"
    type="text"
    placeholder="Name"
    required
  />

  <input
    v-model="age"
    type="number"
    placeholder="Age"
    required
  />

  <input
    v-model="address"
    type="text"
    placeholder="Address"
    required
  />

  <input
    v-model="course"
    type="text"
    placeholder="Course"
    required
  />

  <input
    v-model="year"
    type="text"
    placeholder="Year"
    required
  />

  <h3>Welcome, {{ name }}!</h3>

  <p>Age: {{ age }}</p>
  <p>Address: {{ address }}</p>
  <p>Course: {{ course }}</p>
  <p>Year: {{ year }}</p>
</template>