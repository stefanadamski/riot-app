<template>
  <div class="navigation">
    <div class="left">
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
    <div class="right">
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

.navigation {
  display: flex;
  justify-content: space-between;
  align-content: center;
  margin-bottom: 20px;
}

.left, .right {
  display: flex;
}

.hamburger-wrap {
  width: 100px;
  height: 100%;
  margin-left: 50px;
  margin-right: 50px;
  display: flex;
  align-items: center;
}

.hamburger-wrap {
  float: right;
  justify-content: flex-end;
}

.hamburger {
  border-radius: 4px;
}

.hamburger:focus {
  outline: none;
}

.dropdown {
  height: 0;
  width: 35vw;
  background: #7445FB;
  transition: height 0.2s ease;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  border-radius: 8px;
  margin-right: 10px;
  box-shadow: 0 0 6px #7445FB ;
}


.dropdown-after {
  height: 140px;
  transition: height 0.4s ease;
  border-radius: 8px;
}

.nav-list {
  list-style: none;
}

.nav-list-item {
  text-align: center;
  color: white;
  padding: 2px 10px;
}

.nav-list-item a {
  color: #FFFFFF;
  text-decoration: none;
  display: flex;
  align-items: center;
  justify-content: center;
}
.link-icon {
  width: 12px !important;
  height: 12px !important;
  margin: 5px !important;
}
</style>
