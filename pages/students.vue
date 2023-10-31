<template>
  <h1 class="primary-heading">Student list</h1>
  <div class="content">
    <ul>
      <StudentItem v-for="(student, index) in data" :key="index" :student="student" :studentIndex="index"
                   @remove-student="removeStudent"/>
    </ul>
  </div>
</template>

<script setup>
import StudentItem from "~/components/StudentItem";

const data = ref("");
//const emit = defineEmits(["remove-student"]);

definePageMeta({
  layout: 'main',
  components: {StudentItem},
  methods: {
    removeStudent(student) {
        const index = this.data.indexOf(student);
        this.data.splice(index, 1);
        // data.value = localStorage.setItem('students', JSON.stringify(this.data));
        // emit("remove-student", studentIndex)
        console.log(data);
    }
  }
})

onBeforeMount(()=> {
  data.value = JSON.parse(localStorage.getItem("students"));
})

//onMounted

//skeleton screen for ux

</script>







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