<script setup>
import { ref } from 'vue';
import Registration from './components/Registration.vue';
import Login from './components/Login.vue';

const currentView = ref('home');

const setView = (view) => {
  currentView.value = view;
};

const items = [
  { id: 1, title: 'Házi buli', date: null, image: '' },
  { id: 2, title: 'Lol meccs', date: null, image: '' },
  { id: 3, title: 'Valami', date: null, image: '' },
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
  <main class="h-100">
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
            <img :src="item.image" alt="Kép helye">
          </div>
          <div class="content">
            <h3>{{ item.title }}</h3>
            <p>Időpont: {{ item.date || '-------------' }}</p>
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

header {
  position: fixed;
}

button,
button:hover {
  margin: 0px 10px;
}
</style>