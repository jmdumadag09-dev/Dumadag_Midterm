<script setup>
import { ref } from "vue";
import Form from "./components/Midterm/Form.vue";
import Display from "./components/Midterm/Display.vue";

const student = ref({
  studentName: "",
  studentId: "",
  email: "",
  course: "",
  rating: "",
  recommendation: false,
  feedback: "",
});

function receiveStudent(studentData) {
  student.studentName = studentData.studentName;
  student.studentId = studentData.studentId;
  student.email = studentData.email;
  student.course = studentData.course;
  student.rating = studentData.rating;
  student.recommendation = studentData.recommendation;
  student.feedback = studentData.feedback;
}
</script>

<template>
  <div>
    <h1>Student Feedback System</h1>

    <Form @submit="receiveStudent" />

    <Display :student="student" />
  </div>
</template>