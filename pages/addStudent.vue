<template>
  <AppHeader/>
  <h1 class="primary-heading">Add student</h1>
  <div class="content">
    <StudentForm @add-student="addStudent"/>
  </div>
  <BottomPanel/>
</template>

<script>
import studentForm from "~/components/StudentForm";

export default {
  components: {studentForm},
  data() {
    return {
      students: JSON.parse(sessionStorage.getItem('students')) || []
    }
  },
  methods: {
    addStudent(student) {
      this.students.push(student);
      sessionStorage.setItem('students', JSON.stringify(this.students));
    }
  }

}
</script>