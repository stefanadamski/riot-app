<template>
  <div class="coin">
      <div style="display: flex; width: 200px">
        <div class="coin-logo" style="display: flex">
          <div class="currency-logo-bitcoin"></div>
        </div>
        <div style="display: flex; flex-direction: column">
          <div class="currency-grey-title">BTC</div>
          <div class="currency-black-value">Bitcoin</div>
        </div>
      </div>
      <div style="display: flex; flex-direction: column">
        <div class="currency-grey-title">Price</div>
        <div class="currency-black-value">$17.234</div>
      </div>
      <div style="display: flex; flex-direction: column">
        <div class="currency-grey-title">Change</div>
        <div class="currency-black-value change-up" style="display: flex; justify-content: center; align-items: center">
          <div class="change-icon-small icon-up"></div> + 2% </div>
      </div>
      <div class="coin-chart">
        <img src="https://s3.coinmarketcap.com/generated/sparklines/web/7d/2781/1.svg" alt="bitcoin-7d-price-graph">
      </div>
      <div style="display: flex">
        <button class="buy-sell-buttons transparent-button"> Sell </button>
        <button class="buy-sell-buttons blue-button"> Buy </button>
      </div>
    </div>
    <div class="coin">
      <div style="display: flex; width: 200px">
        <div class="coin-logo" style="display: flex">
          <div class="currency-logo-ethereum"></div>
        </div>
        <div style="display: flex; flex-direction: column">
          <div class="currency-grey-title">ETH</div>
          <div class="currency-black-value">Ethereum</div>
        </div>
      </div>
      <div style="display: flex; flex-direction: column">
        <div class="currency-grey-title">Price</div>
        <div class="currency-black-value">$1.234 </div>
      </div>
      <div style="display: flex; flex-direction: column">
        <div class="currency-grey-title">Change</div>
        <div class="currency-black-value change-down" style="display: flex; justify-content: center; align-items: center">
          <div class="change-icon-small icon-down"></div> - 1.2% </div>
      </div>
      <div class="coin-chart">
        <img src="https://s3.coinmarketcap.com/generated/sparklines/web/7d/2781/1027.svg" class="eth-chart"  alt="ethereum-7d-price-graph" >
      </div>
      <div style="display: flex">
        <button class="buy-sell-buttons transparent-button"> Sell </button>
        <button class="buy-sell-buttons blue-button"> Buy </button>
      </div>
    </div>
</template>

<script>

export default {
  name: "Tab-Temp",
}
</script>

<style scoped>

.coin-chart {
  width: 110px;
  height: 48px;
  margin: 5px;
  filter: contrast(0) sepia(100%) hue-rotate(108deg) brightness(1.2) saturate(0.92);
}

</style>
