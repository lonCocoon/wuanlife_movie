<template>
  <div class="app-wrapper">
    <div class="navbar-wrapper">
      <navbar></navbar>
    </div>
    <div class="main-container">
      <app-main></app-main>
    </div>
  </div>
</template>

<script>
import { Navbar, AppMain } from 'views/layout'

export default {
  name: 'layout',
  components: {
    Navbar,
    AppMain
  },
  computed: {}
}
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
.app-wrapper {
  @include clearfix;
  position: fixed;
  top:0;
  height: 100%;
  width: 100%;
  min-width: 1000px;
  .navbar-wrapper {
    z-index: 100;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #f8f9fa;
  }
  .main-container {
    margin-top: 128px;
    background-color: #f8f9fa;
    height: calc(100vh - #{$nav-height - 22px});
    overflow: auto;
    transition: all 0.28s ease-out;
    padding-bottom: 60px;
  }
}
</style>
