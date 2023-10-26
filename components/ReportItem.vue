<template>
  <li class="report">
    <div class="report-left">
      <img class="report-pfp" src="~/assets/images/pfp.png" alt="Profile picture">
      <div class="info">
        <p class="date">12:38 am - October 17</p>
        <p class="report-name">{{ reportName }}</p>
        <p class="title">{{ title }}</p>
      </div>
    </div>
    <div class="report-right">
      <p class="description">{{ description }}</p>
      <p class="status">{{ status }}</p>
      <p class="time">{{ time }}</p>
      <div class="icons">
        <NuxtLink to="/report">
          <Icon name="ic:baseline-edit"/>
        </NuxtLink>
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
      description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.",
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
  margin-right: 7vw;
}

.report-pfp {
  width: 70px;
  border-radius: 100%;
}

.info {
  margin-left: 40px;
  width: 250px;
}

.date {
  display: none;
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
  max-width: 30vw;
  font-size: 20px;
  opacity: 0.5;
  display: -webkit-box;
  cursor: pointer;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
}

.status {
  font-size: 20px;
  opacity: 0.5;
  padding-left: 10px;
  padding-right: 5px;
}

.time {
  font-size: 20px;
  opacity: 0.5;
  text-align: center;
  padding-left: 5px;
  padding-right: 10px;
}

.icons {
  display: flex;

  a {
    color: black;
  }

  .icon:first-child {
    cursor: pointer;
    margin-right: 5px;
  }

  .icon:last-child {
    cursor: pointer;
    margin-left: 5px;
  }
}

//Media queries

/* Medium devices (tablets, less than 992px) */
@media only screen and (max-width: 991.98px) {
  .report {
    height: 90px;
    margin-bottom: 15px;
  }

  .report-left {
    margin-right: 5vw;
  }

  .report-pfp {
    width: 65px;
  }

  .info {
    margin-left: 20px;
    width: 200px;
  }

  .report-name {
    font-size: 20px;
  }

  .title {
    font-size: 16px;
  }

  .description {
    max-width: 400px;
    font-size: 16px;
  }

  .status {
    display: none;
  }

  .time {
    font-size: 16px;
    padding-left: 10px;
  }
}

/* Medium devices (tablets, 768px and up) */
@media (max-width: 768px) {
  .report-right {
    justify-content: end;
  }

  .description {
    display: none;
  }
}

/* X-Small devices (portrait phones, less than 576px) */
@media only screen and (max-width: 575.98px) {
  .report {
    height: 70px;
    margin-bottom: 10px;
  }

  .report-pfp {
    width: 50px;
  }

  .info {
    width: 150px;
  }

  .date {
    display: flex;
    font-size: 8px;
    opacity: 0.6;
  }

  .report-name {
    font-size: 14px;
  }

  .title {
    font-size: 12px;
  }

  .report-right {
    justify-content: end;
  }

  .description {
    display: none;
  }

  .status {
    display: none;
  }

  .time {
    display: none;
  }
}

/* Extra small devices (portrait phones, less than 380px) */
@media only screen and (max-width: 380px) {
  .report-left {
    display: flex;
    justify-content: space-between;
    width: 100%;
    margin: 0;
  }

  .report-right {
    display: none;
  }
}

</style>