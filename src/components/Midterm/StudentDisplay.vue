<script setup>
const props = defineProps({
  student: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div class="display-container">
    <h2>Submitted Student</h2>

    <p>
      <strong>Student Name:</strong>
      {{ props.student.studentName }}
    </p>

    <p>
      <strong>Student ID:</strong>
      {{ props.student.studentId }}
    </p>

    <p>
      <strong>Email:</strong>
      {{ props.student.email }}
    </p>

    <p>
      <strong>Course:</strong>
      {{ props.student.course }}
    </p>

    <p>
      <strong>Year Level:</strong>
      {{ props.student.yearlevel }}
    </p>
  </div>
</template>