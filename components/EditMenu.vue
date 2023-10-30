<template>
  <div class="container">
    <div class="buttons">
      <button class="btn" @click="isOpen = !isOpen">Status
        <Icon name="material-symbols:keyboard-arrow-down-rounded" :class="{ 'rotate': isOpen }"/>
      </button>
      <div class="dropdown">
        <div v-if="isOpen" class="dropdown-content">
          <ul>
            <li @click="closeDropdown">Open</li>
            <li @click="closeDropdown">In progress</li>
            <li @click="closeDropdown">Close</li>
          </ul>
        </div>
      </div>
      <button class="btn">Print</button>
      <button class="btn">Archive</button>
      <button class="btn btn-save">Save</button>
      <button class="btn btn-delete">Delete</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    }
  },
  methods: {
    closeDropdown() {
      this.isOpen = false;
    }
  }
}

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

.rotate {
  transform: rotate(180deg);
}

.dropdown {
  position: relative;
}

.dropdown-content {
  position: absolute;
  width: 100%;
  background-color: #F1F1F1;
  border-radius: 25px;
  font-size: 20px;
  margin-top: -10px;
  text-align: center;
  z-index: 1;
  cursor: pointer;

  ul {
    list-style-type: none;
  }

  li {
    padding: 15px 0;
    text-decoration: none;
    font-weight: bold;
  }

  li:hover {
    background-color: #E2E2E2;
    border-radius: 25px;
  }
}

.show {
  display: block;
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