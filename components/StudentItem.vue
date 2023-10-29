<template>
  <li class="student-card">
    <div class="student-left">
      <Icon name="ph:student-bold"/>
      <div class="student-info">
        <p class="student-name"><span>Student's name:</span> {{ form.name }}</p>
        <p class="birth"><span>Date of birth:</span> {{ form.birth }}</p>
        <p class="album"><span>Album number:</span> {{ form.album }}</p>
        <p class="field"><span>Field of study:</span> {{ form.field }}</p>
        <p class="email"><span>Email:</span> {{ form.email }}</p>
        <p class="speciality"><span>Specialization:</span> {{ form.speciality }}</p>
      </div>
    </div>
    <div class="student-right">
      <Icon name="ic:baseline-delete" @click="$emit('remove-student', form)"/>
    </div>
  </li>
</template>

<script>
export default {
  props: {
    form: {
      type: Object,
      required: true
    }
  }
  /*data() {
    return {
      studentName: "Bartek Bartowicz",
      album: "123456",
      email: "bartekbartowicz@mail.com",
      birth: "01.01.2000",
      field: "Computer Science",
      speciality: "Front-end developer"
    }
  }*/
}
</script>

<style scoped lang="scss">
.student-card {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #F1F1F1;
  border-radius: 20px;
  padding: 0 20px;
  margin-bottom: 20px;
  height: 100px;
}

.student-left {
  display: flex;
  align-items: center;
}

.student-info {
  margin-left: 40px;
  display: grid;
  grid-template-columns: auto auto;
  grid-gap: 5px 30px;
  align-items: center;
  font-size: 20px;
}

span {
  font-weight: bold;
}

.student-right {
  cursor: pointer;
}

.icon {
  flex-shrink: 0;
}

//Media queries

/* Medium devices (tablets, less than 992px) */
@media only screen and (max-width: 991.98px) {
  .student-card {
    height: 90px;
  }

  .student-info {
    font-size: 16px;
    grid-column-gap: 20px;
  }
}

/* Small devices (landscape phones, less than 768px) */
@media (max-width: 767.98px) {
  .student-info {
    grid-column-gap: 10px;
    grid-template-areas: "column-1 column-2" "column-3 column-4";
  }

  .student-name {
    grid-area: column-1;
  }

  .album {
    grid-area: column-3;
  }

  .field {
    grid-area: column-2;
  }

  .speciality {
    grid-area: column-4;
  }

  .birth, .email {
    display: none;
  }
}

/* X-Small devices (portrait phones, less than 576px) */
@media only screen and (max-width: 575.98px) {
  .student-card {
    height: 70px;
  }

  .student-info {
    display: block;
  }

  .birth, .email, .field, .speciality {
    display: none;
  }
}

/* Extra small devices (portrait phones, less than 380px) */
@media only screen and (max-width: 379.98px) {
  .student-info {
    font-size: 14px;
  }
}
</style>