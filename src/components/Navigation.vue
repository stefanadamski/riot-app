<template>
  <div class="navigation">
    <div class="left-nav">
      <div class="logo">
        <div class="logo-icon"></div>
        <div class="app-name"> Payte </div>
      </div>
      <div class="search-group">
        <div class="search-icon"></div>
        <input type="search" id="site-search" name="search" class="search-input" placeholder="Search">
      </div>
    </div>
    <div class="row dropdown" :class="{ 'dropdown-after' : menuOpen }">
      <ul class="nav-list">
        <li class="nav-list-item">
          <a href="#">Your watchlist<div class="change-icon link-icon"></div></a>
        </li>
        <li class="nav-list-item">
          <a href="#">Community<div class="change-icon link-icon"></div></a>
        </li>
        <li class="nav-list-item">
          <a href="#">Contact Us<div class="change-icon link-icon"></div></a>
        </li>
      </ul>
    </div>
    <div class="right-nav">
      <div class="alerts">
        <div class="alerts-icon"><div class="stroke-icon"></div></div>
      </div>
      <div class="ellipse-icon"></div>
      <div class="hamburger-menu" @click="menuOpen = !menuOpen">
        <div class="hamburger-wrap">
          <div class="hamburger hamburger-icon"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: "Main-Nav",
  components: {},
  data() {
    return {
      menuOpen: false
    }
  }
}
</script>

<style scoped>

</style>
