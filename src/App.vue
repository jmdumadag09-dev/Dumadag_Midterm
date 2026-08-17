<script setup>
import WelcomeForm from "./WelcomeForm.vue";
import RegistrationForm from "./RegistrationForm.vue";
import WcForm from "./components/WcForm.vue";
import Regform from "./components/Regform.vue";


const student = {
  name: "Jian",
  age: 20,
  address: "Bohol",
  course: "if care",
  year: "3rd Year"
};

const studentInfo = {
  course: "BS Information Technology",
  year: "3rd Year"
};


function saveUser(user) {
  console.log("User saved:", user);
  alert("User registered successfully!");
}

function saveStudent(student) {
  console.log("Student saved:", student);
  alert("Student registered successfully!");
}
</script>

<template>

    <WcForm
    :name="student.name"
    :age="student.age"
    :address="student.address"
    :course="student.course"
    :year="student.year"
  />

  <hr />

  <Regform
    @submit="saveStudent"
  />
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