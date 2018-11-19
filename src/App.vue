<!--1.模板：html-->
<template>
  <div id="app">
    <ul>
      <li>
        <router-link to="/">home</router-link>
      </li>
      <li>
        <router-link to="/helloworld">helloworld</router-link>
      </li>
    </ul>
    <router-view></router-view>
  </div>
</template>
<!--2.行为：处理逻辑-->
<script>
export default {
  name: 'App',
  methods: {},
  components: {}
}
</script>


<!--3.样式：解决样式-->
<style scoped>
h1{
  color: purple;
}
</style>
