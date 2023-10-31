<template>
  <div class="container">
    <div class="custom-shape-divider-top-1697724837">
      <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
        <path d="M1200 120L0 16.48 0 0 1200 0 1200 120z" class="shape-fill"></path>
      </svg>
    </div>
    <img src="~/assets/images/logo.png" class="logo" alt="logo">
    <form @submit.prevent="auth">
      <label for="login"></label>
      <input v-model="login" type="text" class="form-group" id="login" placeholder="Login" required>
      <label for="password"></label>
      <input v-model="password" type="password" class="form-group" id="password" placeholder="Password" required>
      <button type="submit" class="btn form-group">Log in</button>
    </form>
  </div>
</template>

<style scoped lang="scss">
@import "~/assets/scss/login";
</style>

<script>
definePageMeta({
  layout: 'main'
})

export default {
  data() {
    return {
      login: '',
      password: '',
    };
  },
  methods: {
    validate() {
      return this.login !== '' && this.password !== '';
    },
    auth() {
      if (this.validate()) {
        this.$router.push('/home');
      }
    }
  }
}
</script>
