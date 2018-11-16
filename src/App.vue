<!--1.模板：html-->
<template>
  <div id="app">
    <app-header></app-header>
    <users v-bind:users="users"></users>
    <app-footer></app-footer>
  </div>
</template>
<!--2.行为：处理逻辑-->
<script>
  import Users from './components/Users'
  import Header from './components/Header'
  import Footer from './components/Footer'
export default {
  name: 'App',
  data(){
    return {
      users:[
        {name:"张启阳",position:"java开发",show:false},
        {name:"张启阳",position:"java开发",show:false},
        {name:"张启阳",position:"java开发",show:false},
        {name:"张启阳",position:"java开发",show:false},
        {name:"张启阳",position:"java开发",show:false},
        {name:"张启阳",position:"java开发",show:false},
        {name:"张启阳",position:"java开发",show:false},
        {name:"张启阳",position:"java开发",show:false},
        {name:"张启阳",position:"java开发",show:false}
      ]
    }
  },
  components:{
    "users":Users,
    "app-header":Header,
    "app-footer":Footer
  }
}
</script>


<!--3.样式：解决样式-->
<style scoped>
h1{
  color: purple;
}
</style>
