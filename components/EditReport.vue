<template>
  <div class="report">
    <div class="upper-info">
      <div class="report-left">
        <img class="report-pfp" src="~/assets/images/pfp.png" alt="Profile picture">
        <div class="info">
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
      description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.",
    }
  }
}
</script>

<style scoped lang="scss">
.report {
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
</style>
