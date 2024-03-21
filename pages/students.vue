<template>
  <AppHeader/>
  <h1 class="primary-heading">Student list</h1>
  <div class="content">
    <ul>
      <StudentItem v-for="student in students" :key="student.name" :student="student"
                   @remove-student="removeStudent"/>
    </ul>
  </div>
  <BottomPanel/>
</template>

<script>
import StudentItem from "~/components/StudentItem";

export default {
  components: {StudentItem},
  data() {
    return {
      students: JSON.parse(sessionStorage.getItem('students')) || []
    }
  },
  methods: {
    removeStudent(student) {
      const index = this.students.indexOf(student);
      this.students.splice(index, 1);
      sessionStorage.setItem('students', JSON.stringify(this.students));
    }
  }
}
</script>