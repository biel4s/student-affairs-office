<template>
  <nav class="navbar">
    <div class="nav-left">
      <p class="nav-name">{{ this.fullName }}</p>
      <p class="id">ID: {{ this.id }}</p>
    </div>
    <div class="nav-right">
      <img class="nav-pfp" src="~/assets/images/pfp.png" alt="Profile picture">
    </div>
  </nav>
  <h1 class="primary-heading">Reports</h1>
  <div class="content">
    <ul>
      <li class="report">
        <div class="report-left">
          <img class="report-pfp" src="~/assets/images/pfp.png" alt="Profile picture">
          <div class="info">
            <p class="report-name">Justyna Justynowicz</p>
            <p class="title">Problem z monitorem</p>
          </div>
        </div>
        <div class="report-right">
          <p class="description">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
            incididunt
            ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis et ut nostrud exercitation ullamco et dolore
            magna aliqua..</p>
          <p class="status">Open</p>
          <p class="time">12:38 am</p>
          <div class="icons">
            <!--<Icon name="logos:apple" fill="#97a3b6"></Icon>-->
            <p>edit</p>
            <p>delete</p>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fullName: "Anna Ankowska",
      id: 123456
    }
  }
}
</script>