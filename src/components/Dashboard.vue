<template>
  <div class="dashboard">
    <Navigation/>
    <div class="container">
      <div class="row dashboard-panel">
        <div class="col-lg-6" style="margin-bottom: 20px">
          <SummaryComponent/>
        </div>
        <div class="col-lg-6" style="margin-bottom: 20px">
          <ChartComponent/>
        </div>
      </div>
      <div class="row dashboard-panel">
        <div class="col-12">
          <DashboardTabs/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SummaryComponent from "@/components/Summary";
import ChartComponent from "@/components/Chart";
import DashboardTabs from "@/components/Tabs";
import Navigation from "@/components/Navigation";


export default {
  name: "Dashboard-Component",
  components: { Navigation, DashboardTabs, ChartComponent, SummaryComponent}
}
</script>

<style scoped>

</style>
