<template>
  <button class="button" @click='getRoute'>getRoute</button>
  <button class="button" @click='push'>push</button>
  <button class="button" @click='replace'>replace</button>
  <button class="button" @click='go'>Go</button>
  <hr/>
  <button class="button" @click='addRoute'>新增路由</button>
</template>
<!-- eslint-disable -->
<script>
export default {
  methods: {
    push(){
      this.$router.push({
        name: 'about'
      });
    },
    replace(){
      this.$router.replace({
        name: 'about'
      });
    },
    go(){
      this.$router.go(-2);
    },
    getRoute(){
    console.log(this.$route);
    },
    addRoute(){
      this.$router.addRoute(
        {
          path: '/newabout',
          name: 'newabout',
          component: () => import('../views/AboutView.vue')
        }
      );
    }
  }
}
</script>