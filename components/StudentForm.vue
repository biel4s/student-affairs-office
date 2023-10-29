<template>
  <div class="container">
    <form @submit.prevent="addStudent">
      <label for="name">Name</label>
      <input v-model="newStudent.name" type="text" class="form-group" id="name" placeholder="Kamil" required>
      <label for="surname">Surname</label>
      <input v-model="newStudent.surname" type="text" class="form-group" id="surname" placeholder="Kamilowicz" required>
      <label for="birth">Date of birth</label>
      <input v-model="newStudent.birth" type="text" class="form-group" id="birth" placeholder="01.01.2000" required>
      <label for="email">Email</label>
      <input v-model="newStudent.email" type="email" class="form-group" id="email"
             placeholder="kamil.kamilowicz@mail.com"
             required>
      <label for="album">Album number</label>
      <input v-model="newStudent.album" type="number" class="form-group" id="album" placeholder="123456" required>
      <label for="field">Field of study</label>
      <input v-model="newStudent.field" type="text" class="form-group" id="field" placeholder="Computer Science"
             required>
      <label for="speciality">Speciality</label>
      <input v-model="newStudent.speciality" type="text" class="form-group" id="speciality"
             placeholder="Front-end developer"
             required>
      <div class="buttons">
        <button type="reset" class="btn btn-reset">Clear</button>
        <button type="submit" class="btn btn-submit">Add</button>
      </div>
    </form>
  </div>
</template>
<script>
export default {
  data() {
    return {
      newStudent: {
        name: '',
        surname: '',
        birth: '',
        email: '',
        album: '',
        field: '',
        speciality: ''
      }
    }
  },
  methods: {
    addStudent() {
      this.$emit('add-student', {...this.newStudent})
      this.newStudent.name = ''
      this.newStudent.surname = ''
      this.newStudent.birth = ''
      this.newStudent.email = ''
      this.newStudent.album = ''
      this.newStudent.field = ''
      this.newStudent.speciality = ''
      //this.$router.push('/home');
    }
  }
}
</script>

<style scoped lang="scss">
@import "assets/scss/variables";

.container {
  display: flex;
  justify-content: center;
  align-items: center;
}

form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 575px;
}

.form-group {
  display: flex;
  height: 50px;
  padding: 10px;
  margin-bottom: 10px;
  border: none;
  border-radius: 15px;
  transition: ease-in-out 0.2s;

}

input {
  box-sizing: border-box;
  padding-left: 20px !important;
  font-size: 1.3rem;
  background: #F1F1F1;
}

input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

label {
  text-align: start;
  font-weight: bold;
}

.buttons {
  display: inline-flex;
}

.btn-reset {
  background-color: #E2E2E2;
  color: black;
  margin-right: 15px;
  width: 50%;
}

.btn-submit {
  background-color: $primary-color;
  margin-left: 15px;
  width: 50%;
}

//Media queries

/* Medium devices (tablets, less than 992px) */
@media only screen and (max-width: 991.98px) {
  form {
    min-width: 500px;
  }

  .form-group {
    height: 45px;
  }
}

/* X-Small devices (portrait phones, less than 576px) */
@media only screen and (max-width: 575.98px) {
  form {
    min-width: 250px;
  }
}
</style>