<template>
  <div>
    <div style="background:red; width: 100px">
      <div>{{ coins }}</div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: "Get-Coins",
  data () {
    return {
      coins: [],
    }
  },
  mounted () {
    axios
        .get('http://localhost:8080/v1/cryptocurrency/latest', {
          headers: {
            'X-CMC_PRO_API_KEY': '240cb6ab-451d-4ede-86e1-6d06d2b9a816',
          },})
        .then(response => (this.coins = response.data))
  }
}
</script>

<style scoped>

</style>
