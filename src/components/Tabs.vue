<template>
  <div class="tabs-component dashboard-element">
    <div class="main-menu">
      <div class="tabs">
        <div class="tab-button" @click="currentTabComponent = 'SummaryTab'">
          Summary
        </div>
        <div class="tab-button" @click="currentTabComponent = 'TableTab'">
          Table
        </div>
        <div class="tab-button" @click="currentTabComponent = 'ChartsTab'">
          Charts
        </div>
        <div class="tab-button" @click="currentTabComponent = 'ReportingTab'">
          Reporting
        </div>
        <div class="tab-button" @click="currentTabComponent = 'AnalysisTab'">
          Analysis
        </div>
      </div>
    </div>
    <div class="content">
      <keep-alive>
        <SummaryTab v-show="currentTabComponent === 'SummaryTab'" class="tab-content"/>
      </keep-alive>
      <keep-alive>
        <TableTab v-show="currentTabComponent === 'TableTab'" class="tab-content"/>
      </keep-alive>
      <keep-alive>
        <ChartsTab v-show="currentTabComponent === 'ChartsTab'" class="tab-content"/>
      </keep-alive>
      <keep-alive>
        <ReportingTab v-show="currentTabComponent === 'ReportingTab'" class="tab-content"/>
      </keep-alive>
      <keep-alive>
        <AnalysisTab v-show="currentTabComponent === 'AnalysisTab'" class="tab-content"/>
      </keep-alive>
    </div>
  </div>
</template>

<script>
import TableTab from "@/components/Tabs/TableTab";
import ChartsTab from "@/components/Tabs/ChartsTab";
import ReportingTab from "@/components/Tabs/ReportingTab";
import AnalysisTab from "@/components/Tabs/AnalysisTab";
import SummaryTab from "@/components/Tabs/SummaryTabAPI";

export default {
  name: "Dashboard-Tabs",
  components: { SummaryTab, AnalysisTab, ReportingTab, ChartsTab, TableTab },
  data() {
    return {
      currentTabComponent: "SummaryTab",
    };
  }
}
</script>

<style scoped>

</style>
