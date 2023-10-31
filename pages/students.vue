<template>
  <h1 class="primary-heading">Student list</h1>
  <div class="content">
    <ul>
      <StudentItem v-for="student in students" :key="student.name" :student="student"
                   @remove-student="removeStudent"/>
    </ul>
  </div>
</template>

<script>
import StudentItem from "~/components/StudentItem";

definePageMeta({
  layout: 'main'
})

export default {
  components: {StudentItem},
  data() {
    return {
      students: JSON.parse(sessionStorage.getItem('students')) || []
      /*students: [
        {
          name: "Bartek Bartowicz",
          birth: "01.01.2000",
          email: "bartekbartowicz@mail.com",
          album: "123456",
          field: "Computer Science",
          speciality: "Front-end developer"
        },
        {
          name: "Bartek Borowicz",
          birth: "01.01.2000",
          email: "bartekbartowicz@mail.com",
          album: "123456",
          field: "Computer Science",
          speciality: "Front-end developer"
        }
      ]*/
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