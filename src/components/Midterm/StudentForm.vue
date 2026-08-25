<script setup>
import { ref } from "vue";

const studentName = ref("Jian Gwapo");
const studentId = ref("18102");
const email = ref("jmd@email.com");
const course = ref("i care");
const yearlevel = ref("yearner 3rd year");

const emit = defineEmits(["submit-student"]);

function submitStudent() {
  const student = {
    studentName: studentName.value,
    studentId: studentId.value,
    email: email.value,
    course: course.value,
    yearlevel: yearlevel.value,
    
  };

  emit("submit-student", student);
}
</script>

<template>
  <div class="form-container">
    <h2>Student Submittion Form</h2>

    <form @submit.prevent="submitStudent">

    
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
        <option value="BSCS">BSCS</option>
        <option value="BSIS">BSIS</option>
      </select>

      
      <label>Year Level Options</label>

      <div>
        <input
          type="radio"
          value="1"
          v-model="yearlevel"
        />
      First Year
      </div>

      <div>
        <input
          type="radio"
          value="2"
          v-model="yearlevel"
        />
        Second Year
      </div>

      <div>
        <input
          type="radio"
          value="3"
          v-model="yearlevel"
        />
        Third Year
      </div>

      <div>
        <input
          type="radio"
          value="4"
          v-model="yearlevel"
        />
        Fourth Year
      </div>


     

        <button type="submit">Submit Student</button>

    </form>
  </div>
</template>