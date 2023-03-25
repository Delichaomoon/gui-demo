<template>
  <nav class="mb-5 navbar navbar-expand-lg navbar-light bg-light fixed-top">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <router-link to="/" class="nav-link">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/about" class="nav-link">About</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/newPage" class="nav-link">newPage</router-link>
        </li>
      </ul>
    </div>
  </div>
  </nav>
  <div class="container" style="height:300vh">
    <router-view/>
    {{ name }}
  </div>
  <router-link to="/newPage/routerNavigation">路由導覽</router-link>
</template>

<style lang="scss">
@import "bootstrap";
</style>

<script>
/* eslint-disable */
  export default {
    data(){
      return{
        name: process.env.VUE_APP_NAME,
      }
    }
  }
</script>