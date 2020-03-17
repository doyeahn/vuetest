<template>
   <div  id="App">
      <div>  
        <nav>
          <ul>
            <li>
              <router-link v-bind:to="{name:'home'}">홈</router-link></li>
            <li @click="time" v-bind:to="{name:'time'}">시간</li>
            <li><router-link v-bind:to="{name: 'search'}">검색</router-link></li>
        </ul>
        </nav>
    </div>
    <div>
      <router-view></router-view>
    </div>
    </div>
</template>

<script>

//import Home from './components/Home.vue'
//import Time from './components/Time.vue'
import Search from './components/Search.vue'
import VueRouter from 'vue-router'
//import Login from './components/Login.vue'

export default {
  name: 'App', router,
  components: {
 Search//, Time, Login

 }

}

const router = new VueRouter({
  routes : [
   // {path: '/', component: Home},
  //  {path:'/home', name:'home', component: Home},
   // {path:'/time', name:'time', component: Time},
    {path: '/search', name:'search', component: Search} //,
    //{path: '/login', name:'login', component: Login}
    //beforeRouteEnter: (to, from, next)=>{}
  ]
  
})
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.nav {float: left; width: 200px;}

</style>
