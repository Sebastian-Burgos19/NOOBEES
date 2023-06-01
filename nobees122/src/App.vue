<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>

  <div id="app">
  <nav>
  <ul>
  <li><router-link to="/">Inicio</router-link></li>
  <li><router-link to="/opcion1">Opcion 1</router-link></li>
  <li><router-link to="/opcion2">Opcion 2</router-link></li>
  <li><router-link to="/opcion3">Opcion 3</router-link></li>
  </ul>
  </nav>
  <router-view></router-view>
  </div>
</template>

<script>

import { createRouter, createWebHistory } from 'vue-router';
import Inicio from './components/Inicio.vue';
import Opcion1 from './components/Opcion1.vue';
import Opcion2 from './components/Opcion2.vue';
import Opcion3 from './components/Opcion3.vue';

const routes = [
 {
 path: '/',
 name: 'inicio',
 component: Inicio
 },
 {
 path: '/opcion1',
 name: 'opcion1',
 component: Opcion1
 },
 {
 path: '/opcion2',
 name: 'opcion2',
 component: Opcion2
 },
 {
 path: '/opcion3',
 name: 'opcion3',
 component: Opcion3
 }
];
const router = createRouter({
 history: createWebHistory(),
 routes
});
export default router;
</script>



 <style>
 #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  margin-top: 60px;
 }
 ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
 }
li {
 margin-bottom: 10px;
}
a {
 text-decoration: none;
}
</style>