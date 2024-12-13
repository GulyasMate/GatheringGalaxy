<script setup>
//bootstrap
import "bootstrap/dist/css/bootstrap.min.css";
import "bootstrap/dist/js/bootstrap.bundle.min.js";
//functions
import { ref } from 'vue';
//components
import Registration from './components/Registration.vue';
import Login from './components/Login.vue';

const currentView = ref('home');

const setView = (view) => {
  currentView.value = view;
};

const getImgFromURL = (url) => {
  return new URL(url, import.meta.url).href;
}

const items = [
  { id: 1, title: 'Házi buli', date: null, image: './assets/dummy.png' },
  { id: 2, title: 'Lol meccs', date: null, image: './assets/dummy.png' },
  { id: 3, title: 'Valami', date: null, image: './assets/dummy.png' },
];
</script>

<template>
  <header class="w-100">
    <nav class="navbar">
      <div class="container-fluid">
        <a class="navbar-brand" href="#" @click="setView('home')">
          <img src="\src\assets\result.png" alt="Logo" width="30" height="24" class="d-inline-block align-text-top">
          GratheringGalaxy
        </a>
        <div v-if="currentView === 'home'">
          <button @click="setView('login')">Bejelentkezés</button>
          <button @click="setView('registration')">Regisztráció</button>
        </div>
      </div>
    </nav>
  </header>
  <main>
    <div class="container">
      <div v-if="currentView === 'login'">
        <Login />
      </div>
      <div v-if="currentView === 'registration'">
        <Registration />
      </div>
      <div v-if="currentView === 'home'" class="item-list">
        <div v-for="item in items" :key="item.id" class="list-item">
          <div class="image-container">
            <img :src="getImgFromURL(item.image)" alt="Kép helye">
          </div>
          <div class="content">
            <h3>{{ item.title }}</h3>
            <p class="pb-2">Időpont: {{ item.date || '-------------' }}</p>
          </div>
          <div class="action">
            <button @click="showDetails(item.id)">Részletek</button>
          </div>
        </div>
      </div>
    </div>
  </main>
  <footer>
    <p>Copyright &copy;</p>
  </footer>
</template>
<style>
.navbar-brand:hover,
.navbar-brand {
  color: #DFD1EB;
}
button,
button:hover {
  margin: 0px 10px;
}
img {
  width: 100px;
  border-radius: 50%;
}
.list-item{
  margin-bottom: 10px;
  background-color: #1e1e2f;
  padding: 10px 20px;
  border-radius: 10px;
  color: #DFD1EB;
}
p{
  margin-bottom: 0;
}
</style>