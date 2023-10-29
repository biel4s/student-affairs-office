<template>
  <nav class="navbar">
    <div class="nav-info">
      <p class="nav-name">{{ fullName }}</p>
      <p class="id">ID: {{ id }}</p>
    </div>
    <img class="nav-pfp" src="~/assets/images/pfp.png" alt="Profile picture">
  </nav>
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

<style scoped lang="scss">
@import "assets/scss/_variables.scss";

.navbar {
  height: 70px;
  width: 100%;
  background-color: $secondary-color;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-info {
  color: white;
  margin-left: 3rem;
}

.nav-name {
  font-size: 24px;
  font-weight: bold;
}

.nav-pfp {
  border-radius: 100%;
  width: 55px;
  margin-right: 3rem;
}

//Media queries

/* Medium devices (tablets, less than 992px) */
@media only screen and (max-width: 991.98px) {
  .navbar {
    height: 65px;
  }

  .nav-info {
    margin-left: 2rem;
  }

  .nav-name {
    font-size: 20px;
  }

  .id {
    font-size: 14px;
  }

  .nav-pfp {
    width: 50px;
    margin-right: 2rem;
  }
}

/* X-Small devices (portrait phones, less than 576px) */
@media only screen and (max-width: 575.98px) {
  .navbar {
    height: 60px;
  }

  .nav-info {
    margin-left: 1rem;
  }

  .nav-name {
    font-size: 16px;
  }

  .id {
    font-size: 12px;
  }

  .nav-pfp {
    width: 45px;
    margin-right: 1rem;
  }
}
</style>