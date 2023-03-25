<template>
  <div class="row">
    <div class="col-4">
      <div class="list-group">
        <router-link to="/newPage/a" class="list-group-item list-group-item-action">A</router-link>
        <router-link to="/newPage/b" class="list-group-item list-group-item-action">B</router-link>
        <router-link to="/newPage/namedView/c2a" class="list-group-item list-group-item-action">命名視圖C2a</router-link>
        <router-link to="/newPage/namedView/a2b" class="list-group-item list-group-item-action">命名視圖A2B</router-link>
        <router-link to="/newPage/dynamicRouter" class="list-group-item list-group-item-action">動態路由$route</router-link>
        <router-link to="/newPage/dynamicRouterProps" class="list-group-item list-group-item-action">動態路由Props</router-link>
        <router-link to="/newPage/routerNavigation" class="list-group-item list-group-item-action">路由導覽</router-link>
      </div>
    </div>
    <div class="col-8">
      <router-view></router-view>
    </div>
  </div>
</template>
<!--eslint-disable  -->