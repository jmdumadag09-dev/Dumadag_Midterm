<script setup>
import WelcomeForm from "./WelcomeForm.vue";
import RegistrationForm from "./RegistrationForm.vue";

const studentInfo = {
  course: "BS Information Technology",
  year: "3rd Year"
};

function saveUser(user) {
  console.log("User saved:", user);
  alert("User registered successfully!");
}
</script>

<template>
  <WelcomeForm
    :course="studentInfo.course"
    :year="studentInfo.year"
  />

  <hr />

  <RegistrationForm
    :course="studentInfo.course"
    :year="studentInfo.year"
    @submit="saveUser"
  />
</template>