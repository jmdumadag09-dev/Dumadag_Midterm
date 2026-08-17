<script setup>
import { ref } from "vue";

const fname = ref("");
const lname = ref("");
const mi = ref("");
const address = ref("");
const email = ref("");
const birthdate = ref("");
const description = ref("");

const emit = defineEmits(["submit"]);

function submitForm() {
  const user = {
    fname: fname.value,
    lname: lname.value,
    mi: mi.value,
    address: address.value,
    email: email.value,
    birthdate: birthdate.value,
    description: description.value
  };

  emit("submit", user);
}
</script>

<template>
  <h2>Registration Form</h2>

  <form @submit.prevent="submitForm">

    <input
      v-model="fname"
      placeholder="First Name"
      required
    />

    <input
      v-model="lname"
      placeholder="Last Name"
      required
    />

    <input
      v-model="mi"
      placeholder="Middle Initial"
      maxlength="1"
    />

    <input
      v-model="address"
      placeholder="Address"
      required
    />

    <input
      v-model="email"
      type="email"
      placeholder="Email"
      required
    />

    <input
      v-model="birthdate"
      type="date"
      required
    />

    <textarea
      v-model="description"
      placeholder="Short description about myself"
      required
    ></textarea>

    <button type="submit">
      Submit
    </button>

  </form>
</template>