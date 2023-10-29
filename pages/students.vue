<template>
  <AppHeader/>
  <h1 class="primary-heading">Student list</h1>
  <div class="content">
    <ul>
      <StudentItem v-for="student in students" :key="student.name" :form="student" @remove-student="removeStudent"/>
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
      students: [
        {name: "Test", birth: "Test", email: "test", album: "test", field: "test", speciality: "test"},
        {name: "Test1", birth: "Test", email: "test", album: "test", field: "test", speciality: "test"}
      ]
    }
  },
  methods: {
    removeStudent(student) {
      const index = this.students.indexOf(student);
      this.students.splice(index, 1);
    }
  }
}
</script>