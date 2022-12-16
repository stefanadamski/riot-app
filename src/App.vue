<template>
  <Dashboard/>
</template>

<script>
import Dashboard from "@/components/Dashboard";

export default {
  name: 'App',
  components: { Dashboard }
}
</script>

<style>

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #1E1E1E;
  text-align: center;
  width: 100%;
  height: auto;
  min-height: 100vh;
  padding: 10px;
}

</style>
