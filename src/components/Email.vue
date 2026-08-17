<script setup>
import { ref } from 'vue'

const name = ref('')
const email = ref('')

const emit = defineEmits(['submit'])

function submitForm() {
  emit('submit', {
    name: name.value,
    email: email.value
  })
}
</script>

<template>
  <form @submit.prevent="submitForm">
    <h2>Student Form</h2>

    <input
      v-model="name"
      placeholder="Student Name"
      required
    >

    <br><br>

    <input
      v-model="email"
      type="email"
      placeholder="Student Email"
      required
    >

    <br><br>

    <button type="submit">Save Student</button>
  </form>
</template>