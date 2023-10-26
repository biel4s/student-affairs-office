<template>
  <AppHeader/>
  <h1 class="primary-heading">Reports</h1>
  <div class="content">
    <ul>
      <ReportItem/>
      <ReportItem/>
      <ReportItem/>
      <ReportItem/>
      <ReportItem/>
      <ReportItem/>
      <ReportItem/>
    </ul>
  </div>
  <BottomPanel/>
</template>

<script>
import AppHeader from "~/components/AppHeader.vue";

export default {
  components: {AppHeader},
  data() {
    return {
      fullName: "Anna Ankowska",
      id: 123456
    }
  }
}
</script>