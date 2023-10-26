<template>
  <li class="report">
    <div class="report-left">
      <img class="report-pfp" src="~/assets/images/pfp.png" alt="Profile picture">
      <div class="info">
        <p class="report-name">{{ reportName }}</p>
        <p class="title">{{ title }}</p>
      </div>
    </div>
    <div class="report-right">
      <p class="description">{{ description }}</p>
      <p class="status">{{ status }}</p>
      <p class="time">{{ time }}</p>
      <div class="icons">
        <Icon name="ic:baseline-edit"/>
        <Icon name="ic:baseline-delete"/>
      </div>
    </div>
  </li>
</template>

<script>
export default {
  data() {
    return {
      reportName: "Justyna Justynowicz",
      title: "Problem z monitorem",
      description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis et ut nostrud exercitation ullamco et dolore magna aliqua..",
      status: "Open",
      time: "12:38 am"
    }
  }
  /* name: "ReportItem",
  props: {
    reportName: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    status: {
      type: String,
      required: true,
    },
    time: {
      type: String,
      required: true,
    },*/
}
</script>

<style lang="scss">

.report {
  display: flex;
  align-items: center;
  background-color: #F1F1F1;
  border-radius: 20px;
  padding: 0 20px;
  margin-bottom: 20px;
  height: 100px;
}

.report-left {
  display: flex;
  align-items: center;
  margin-right: 150px;
}

.report-pfp {
  width: 70px;
  border-radius: 100%;
}

.info {
  margin-left: 40px;
  width: 250px;
}

.report-name {
  font-weight: bold;
  font-size: 24px;
}

.title {
  font-size: 20px;
}

.report-right {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
}

.description {
  max-width: 700px;
  font-size: 20px;
  opacity: 0.5;
  cursor: pointer;
}

.status {
  font-size: 20px;
  opacity: 0.5;
}

.time {
  font-size: 20px;
  opacity: 0.5;
}

.icons {
  display: flex;

  .icon:first-child {
    cursor: pointer;
    margin-right: 5px;
  }

  .icon:last-child {
    cursor: pointer;
    margin-left: 5px;
  }
}
</style>