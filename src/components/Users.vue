<!--1.模板-->
<template>
    <div class="users">
      <ul>
        <li v-for="user in users">
          <h2>{{user.name}}</h2>
          <h3>{{user.email}}</h3>
        </li>
      </ul>
    </div>

</template>


<!--2.行为-->
<script>
    export default {
        name: 'Users',
      data(){
          return{

          }
      },
      props:{
          users:{
            type:Array,
            require:true
          }
      }
    }
</script>
<!--3.样式-->
<style scoped>
  .users{
    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;
  }
  ul{
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
  }
  li{
    flex-grow: 1;
    flex-basis: 200px;
    text-align: center;
    padding: 30px;
    border: 1px solid #222;
    margin: 10px;
  }
</style>
