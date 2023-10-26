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

.nav-left {
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
</style>