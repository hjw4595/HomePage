<template>
  <div id="app">
    <b-navbar toggleable="md" type="dark">
      </b-navbar>

<b-navbar toggleable="md" type="dark" class="nav">
  <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

  <b-navbar-nav class="ml-auto">
    <h4>머리</h4>
  </b-navbar-nav>

  <b-nav pills>
        <b-nav-item> 
          <router-link to="/mainPage" replace active-class>메인</router-link>
        </b-nav-item>
        <b-nav-item>
          <router-link to="/eventPage" replace>이벤트</router-link>
        </b-nav-item>
           <b-nav-item>
          <router-link to="/reservationPage" replace>예약</router-link>
        </b-nav-item>
  </b-nav>

  <b-collapse is-nav id="nav_collapse">
    <b-navbar-nav class="ml-auto"> 
       <b-nav-item>
       <router-link to="/loginPage" replace>로그인</router-link>
        </b-nav-item>
         <b-nav-item>
        <router-link to="/joinPage" replace>회원가입</router-link>
        </b-nav-item>
    </b-navbar-nav>
  </b-collapse>

</b-navbar>

<router-view></router-view>

  </div>
</template>
<script>
import mainPage from './components/mainPage.vue'

import Vue from 'vue'
import BootstrapVue from 'bootstrap-vue'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

Vue.use(BootstrapVue);
export default {
  name: 'App',
  components: { mainPage}
}
</script>

<style>
 .nav {
    background-color: black;
    color: white;
  }
</style>
