<template>
  <AppHeader/>
  <h1 class="primary-heading">Student list</h1>
  <div class="content">
    <ul>
      <StudentItem/>
      <StudentItem/>
      <StudentItem/>
      <StudentItem/>
      <StudentItem/>
      <!--<StudentItem v-for="student in students" :key="student.name" :student="student"></StudentItem>-->
    </ul>
  </div>
  <BottomPanel/>
</template>

<script>
</script>