<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view/>
  {{ name }}
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