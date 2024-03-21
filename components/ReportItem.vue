<template>
  <li class="report-card">
    <div class="report-left">
      <img class="report-pfp" src="~/assets/images/pfp.png" alt="Profile picture">
      <div class="report-info">
        <p class="date">Today - 12:38 am</p>
        <p class="report-name">{{ report.reportName }}</p>
        <p class="title">{{ report.title }}</p>
      </div>
    </div>
    <div class="report-right">
      <p class="description">{{ report.description }}</p>
      <p class="status">{{ report.status }}</p>
      <p class="time">{{ report.time }}</p>
      <div class="icons">
        <NuxtLink :to="`/report/${reportIndex}`">
          <Icon name="ic:baseline-edit"/>
        </NuxtLink>
        <Icon name="ic:baseline-delete" @click="$emit('remove-report', reportIndex)"/>
      </div>
    </div>
  </li>
</template>

<script>
export default {
  props: {
    report: {
      type: Object,
      required: true
    },
    reportIndex: Number
  }
}
</script>

<style scoped lang="scss">
.report-card {
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

.report-info {
  margin-left: 20px;
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
  .report-card {
    height: 90px;
    margin-bottom: 15px;
  }

  .report-left {
    margin-right: 5vw;
  }

  .report-pfp {
    width: 65px;
  }

  .report-info {
    margin-left: 15px;
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

/* Small devices (landscape phones, less than 768px) */
@media (max-width: 767.98px) {
  .report-right {
    justify-content: end;
  }

  .description {
    display: none;
  }
}

/* X-Small devices (portrait phones, less than 576px) */
@media only screen and (max-width: 575.98px) {
  .report-card {
    height: 70px;
    margin-bottom: 10px;
  }

  .report-pfp {
    width: 50px;
  }

  .report-info {
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
@media only screen and (max-width: 379.98px) {
  .report-card {
    padding: 0 10px;
  }

  .report-left {
    display: flex;
    width: 100%;
    margin: 0;
  }

  .icons {
    svg {
      transform: scale(0.8);
    }
  }
}

</style>