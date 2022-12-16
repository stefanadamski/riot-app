<template>
  <div class="all-coins">
    <TabTemp/>
    <div v-for="coin in coins" v-bind:key="coin.id" class="coin">
      <div style="display: flex">
        <div class="coin-logo" style="display: flex">
          <div class="currency-logo"></div>
        </div>
        <div style="display: flex; flex-direction: column">
          <div class="currency-grey-title">BTC{{ coin.symbol }}</div>
          <div class="currency-black-value">Bitcoin{{ coin.name }}</div>
        </div>
      </div>
      <div style="display: flex; flex-direction: column">
        <div class="currency-grey-title">Price</div>
        <div class="currency-black-value">$17.234{{ coin.price }}</div>
      </div>
      <div style="display: flex; flex-direction: column">
        <div class="currency-grey-title">Change</div>
        <div class="currency-black-value change-small" style="display: flex; justify-content: center; align-items: center">
          <div class="change-icon-small icon-down"></div> - 24% {{ coin.percent_change_24h }}</div>
      </div>
      <div class="coin-chart"></div>
      <div style="display: flex">
        <button class="buy-sell-buttons transparent-button"> Sell </button>
        <button class="buy-sell-buttons blue-button"> Buy </button>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import TabTemp from "@/components/Tabs/SummaryTabTemporary";

export default {
  name: "Summary-Tab",
  components: {TabTemp},
  data () {
    return {
      coins: [],
    }
  },
  mounted () {
    axios
        .get('http://localhost:8080/v1/cryptocurrency/listings/latest', {
          headers: {
            'X-CMC_PRO_API_KEY': '240cb6ab-451d-4ede-86e1-6d06d2b9a816',
          },})
        .then(response => (this.coins = response.data))
        .then(response => console.log(response.data))
  }
}
</script>

<style scoped>

</style>
