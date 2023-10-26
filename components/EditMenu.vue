<template>
  <div class="container">
    <div class="buttons">
      <button class="btn">Status
        <Icon name="material-symbols:keyboard-arrow-down-rounded"/>
      </button>
      <button class="btn">Print</button>
      <button class="btn">Archive</button>
      <button class="btn btn-save">Save</button>
      <button class="btn btn-delete">Delete</button>
    </div>
  </div>
</template>

<script>

</script>

<style scoped lang="scss">
@import "assets/scss/_variables.scss";

.container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.buttons {
  display: flex;
  justify-content: center;
  flex-direction: column;
  width: 600px;
}

.btn {
  color: black;
  height: 60px;
  margin-top: 0;
  margin-bottom: 10px;
  position: relative;
}

.btn-save {
  background-color: $primary-color;
  color: white;
}

.btn-delete {
  background-color: $danger-color;
  color: white;
}

.icon {
  position: absolute;
  right: 0;
  margin-right: 10px;
}

//Media queries

/* Medium devices (tablets, less than 992px) */
@media only screen and (max-width: 991.98px) {
  .buttons {
    width: 450px;
  }

  .btn {
    height: 50px;
    font-size: 20px;
  }
}

/* X-Small devices (portrait phones, less than 576px) */
@media only screen and (max-width: 575.98px) {
  .buttons {
    max-width: 400px;
  }

  .btn {
    height: 40px;
    font-size: 16px;
  }
}
</style>