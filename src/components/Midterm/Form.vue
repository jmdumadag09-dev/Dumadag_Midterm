<script setup>
import { ref } from "vue";

const studentName = ref("");
const studentId = ref("");
const email = ref("");
const course = ref("");
const rating = ref("");
const recommendation = ref(false);
const feedback = ref("");

const emit = defineEmits(["submit"]);

function submitForm() {
  const student = {
    studentName: studentName.value,
    studentId: studentId.value,
    email: email.value,
    course: course.value,
    rating: rating.value,
    recommendation: recommendation.value,
    feedback: feedback.value,
  };

  emit("submit", student);
}
</script>

<template>
  <div class="form-container">
    <h2>Student Feedback Form</h2>

    <form @submit.prevent="submitForm">

    
      <label>Student Name:</label>
      <input
        type="text"
        v-model="studentName"
        required
      />

      <label>Student ID:</label>
      <input
        type="text"
        v-model="studentId"
        required
      />
      <label>Email:</label>
      <input
        type="email"
        v-model="email"
        required
      />

     
      <label>Course:</label>
      <select v-model="course" required>
        <option value="" disabled>Select your course</option>
        <option value="BSIT">BSIT</option>
        <option value="BSHM">BSHM</option>
        <option value="BSBA">BSBA</option>
        <option value="BSN">BSN</option>
        <option value="BSED">BSED</option>
      </select>

      
      <label>Rating:</label>

      <div>
        <input
          type="radio"
          value="1"
          v-model="rating"
        />
      1-looy
      </div>

      <div>
        <input
          type="radio"
          value="2"
          v-model="rating"
        />
        2-di kaayo looy
      </div>

      <div>
        <input
          type="radio"
          value="3"
          v-model="rating"
        />
3-okay
      </div>

      <div>
        <input
          type="radio"
          value="4"
          v-model="rating"
        />
    4-okay kaayo
      </div>

      <div>
        <input
          type="radio"
          value="5"
          v-model="rating"
        />
        5 - kina okayhan
      </div>

      <div>
        <input
          type="checkbox"
          v-model="recommendation"
        />
        I would recommend this course to other students.
      </div>

      
      <label>Feedback:</label>
      <textarea
        v-model="feedback"
        rows="5"
        placeholder="Enter your feedback..."
        required
      ></textarea>

      <button type="submit">Submit Feedback</button>

    </form>
  </div>
</template>