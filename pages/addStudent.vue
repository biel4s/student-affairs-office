<template>
  <h1 class="primary-heading">Add student</h1>
  <div class="content">
    <StudentForm @add-student="addStudent"/>
  </div>
</template>

<script>
import studentForm from "~/components/StudentForm";

definePageMeta({
  layout: 'main'
})

export default {
  components: {studentForm},
  data() {
    return {
      students: JSON.parse(localStorage.getItem('students')) || []
    }
  },
  methods: {
    addStudent(student) {
      if (process.client) {
        this.students.push(student);
        localStorage.setItem('students', JSON.stringify(this.students));
      }
    }
  }

}
</script>