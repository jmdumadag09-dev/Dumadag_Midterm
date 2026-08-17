<script setup>
import { computed } from "vue";

const students = [
  { id: 1, name: "Jian", age: 20 },
  { id: 2, name: "Bro", age: 21 },
  { id: 3, name: "Jed", age: 19 },
];

const totalStudent = computed(() => students.length);

</script>
<template>
  <div v-for="student in students" :key="student.name">
    <p>Student ID: {{ student.id }}</p>
    <p>Name: {{ student.name }}</p>
    <p>Age: {{ student.age }}</p>
  </div>

  <p>Total Students: {{ totalStudent }}</p>
</template>
