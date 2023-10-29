<template>
  <div class="report-card">
    <div class="upper-info">
      <div class="report-left">
        <img class="report-pfp" src="~/assets/images/pfp.png" alt="Profile picture">
        <div class="report-info">
          <p class="date2">{{ date }}</p>
          <p class="report-name">{{ reportName }}</p>
          <p class="title">{{ title }}</p>
        </div>
      </div>
      <div class="report-right">
        <p class="date">{{ date }}</p>
      </div>
    </div>
    <p class="description">{{ description }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      reportName: "Justyna Justynowicz",
      title: "Problem z monitorem",
      date: "12:38 am - October 17",
      description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur."
    }
  }
}
</script>

<style scoped lang="scss">
.report-card {
  height: auto;
  display: flex;
  flex-direction: column;
  padding: 15px 20px;
}

.upper-info {
  display: flex;
  width: 100%;
}

.report-right {
  justify-content: end;
  opacity: 0.7;
}

.date {
  display: flex;
  font-size: 22px;
  text-align: center;
}

.description {
  display: flex;
  margin-top: 30px;
  max-width: 100%;
  opacity: 1;
  font-size: 24px;
  overflow: auto;
  cursor: default;
}

//Media queries

/* Medium devices (tablets, less than 992px) */
@media only screen and (max-width: 991.98px) {
  .report-pfp {
    width: 65px;
  }

  .info {
    width: 250px;
  }

  .report-name {
    font-size: 24px;
  }

  .title {
    font-size: 18px;
  }

  .date {
    font-size: 18px;
  }

  .description {
    margin-top: 25px;
    font-size: 20px
  }
}

/* X-Small devices (portrait phones, less than 576px) */
@media only screen and (max-width: 575.98px) {
  .report-pfp {
    width: 45px;
  }

  .info {
    width: 250px;
  }

  .report-name {
    font-size: 18px;
  }

  .title {
    font-size: 14px;
  }

  .date {
    display: none;
  }

  .date2 {
    font-size: 12px;
    opacity: 0.6;
  }

  .description {
    margin-top: 20px;
    font-size: 16px
  }
}

@media only screen and (min-width: 576px) {
  .date2 {
    display: none;
  }
}
</style>
