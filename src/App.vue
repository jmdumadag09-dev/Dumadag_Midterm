<script setup>
import { ref } from "vue";
import StudentForm from "./components/Midterm/StudentForm.vue";
import StudentDisplay from "./components/Midterm/StudentDisplay.vue";

const student = ref({
  studentName: "Jian Gwapo",
  studentId: "18102",
  email: "jm@gmail.com",
  course: "i care",
  yearlevel: " 3rd yearner",
});

function receiveStudent(studentData) {
  student.value = studentData;
}
</script>

<template>
  <div>
    <h1>Student Submittion System</h1>

    <StudentForm @submit-student="receiveStudent" />

    <StudentDisplay :student="student" />
  </div>
</template>