<template>
  <header @click="changeTitle">
    <h1>{{title1}} {{title}}</h1>
  </header>
</template>

<script>
  export default {
    name: "app-header",
    data(){
      return{
        title1: "Vue.js Demo"
      }
    },
    props:{
      title:{
        type:String
      }

    },
    methods:{
      changeTitle:function () {
        // this.title="changed"
        this.$emit("titleChange","子向父组件传值")
      }
    },
    //生命周期
    // beforeCreate:function(){
    //   alert("组件实例化之前执行的函数");
    // },
    // created:function(){
    //   alert("组件实例化完毕，但页面还未显示");
    // },
    // beforeMount:function () {
    //   alert("组件挂载前，但页面仍未显示，虚拟Dom已经配置");
    // },
    // mounted:function () {
    //   alert("组件挂载后，执行此方法，页面显示");
    // },
    // beforeUpdate:function () {
    //   alert("组件更新前，页面仍未更新，但虚拟Dom已经配置");
    // },
    // updated:function () {
    //   alert("组件更新，执行此方法后，页面更新");
    // },
    // beforeDestroy:function () {
    //   alert("组件销毁前");
    // },
    // destroyed:function () {
    //   alert("组件销毁");
    // }


  }
</script>

<style scoped>
  header{
    background: lightgreen;
    padding: 10px;
  }
  h1{
    color: #222;
    text-align: center;
  }

</style>
