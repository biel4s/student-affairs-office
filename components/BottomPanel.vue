<template>
  <nav class="panel">
    <div class="home">
      <NuxtLink to="/home">
        <Icon name="ic:baseline-home"/>
        <p>Home</p>
      </NuxtLink>
    </div>
    <div class="add-student">
      <NuxtLink to="/addStudent">
        <Icon name="ic:baseline-add-circle-outline"/>
        <p>Add student</p>
      </NuxtLink>
    </div>
    <div class="reports">
      <NuxtLink to="/home">
        <Icon name="ic:twotone-mail-outline"/>
        <p>Reports</p>
      </NuxtLink>
    </div>
  </nav>
</template>

<script setup lang="ts">
</script>

<style scoped lang="scss">
@import "assets/scss/_variables.scss";

/* X-Large devices (large desktops, 1281px and up) */
@media only screen and (min-width: 1281px) {
  .panel {
    display: none;
  }
}

/* Large devices (landscape tablets, desktops, less than 1281px) */
@media only screen and (max-width: 1280.98px) {
  .panel {
    position: fixed;
    bottom: 0;
    display: flex;
    align-items: center;
    text-align: center;
    justify-content: space-evenly;
    height: 60px;
    width: 100%;
    background-color: $primary-color;
  }

  a {
    text-decoration: none;
    color: white;
  }

  .home, .add-student, .reports {
    cursor: pointer;
  }

  p {
    font-size: 14px;
  }
}

/* X-Small devices (portrait phones, less than 576px) */
@media only screen and (max-width: 575.98px) {
  .panel {
    height: 50px;
  }

  p {
    font-size: 12px;
  }
}

</style>