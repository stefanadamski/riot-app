<template>
  <div class="dashboard-element">
    <div style="display: flex; justify-content: space-between">
      <div class="component-header">Current Balance</div>
      <div class="more-info">
        <div class="more-info-icon"></div>
      </div>
    </div>
    <div class="total-balance"><span class="currency-symbol">$</span>21 432.23</div>
    <div style="display: flex; justify-content: flex-start; align-items: center">
      <div class="change">
        <div class="change-icon"></div>
      </div>
      <div class="monthly-change"> 12% vs last month </div>
    </div>
    <div class="button-group">
      <button class="balance-button blue-button"> Quick Invest </button>
      <button class="balance-button transparent-button"> Show Report </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Summary-Component"
}
</script>

<style scoped>

</style>
