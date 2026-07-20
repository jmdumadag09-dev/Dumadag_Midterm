<script>
import EcmaBind from "./components/EcmaBind.vue";

export default {
  components: {
    EcmaBind,
  },
};
</script>

<template>
  <div>
    <EcmaBind studentName="Jian" course="BIST" :isEnrolled="true" />

    <EcmaBind
      studentName="Aljon"
      course="BSIT"
      :isEnrolled="false" />

    <EcmaBind
      studentName="Alaniel"
      course="BSIT"
      :isEnrolled="true" />
  </div>
</template>
