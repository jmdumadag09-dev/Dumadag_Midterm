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
    <h2>Submitted Feedback</h2>

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
      <strong>Rating:</strong>
      {{ props.student.rating }}
    </p>

    <p>
      <strong>Would Recommend:</strong>
      {{ props.student.recommendation ? "Yes" : "No" }}
    </p>

    <p>
      <strong>Feedback:</strong>
      {{ props.student.feedback }}
    </p>
  </div>
</template>