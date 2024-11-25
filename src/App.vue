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

const showDetails = (id) => {
  console.log('Részletek:', id);
};
</script>

<template>
  <div class="app-container">
    <header>
      <img 
        src="/src/assets/result.png" 
        alt="GatheringGalaxy" 
        title="Gathering Galaxy"
        @click="setView('home')" 
        style="cursor: pointer;"
      >
      <h1>GatheringGalaxy</h1>
    </header>
    <main>
      <div v-if="currentView === 'home'">
        <button @click="setView('login')">Login</button>
        <button @click="setView('registration')">Register</button>
      </div>
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
    </main>
    <footer>
      <p>Copyright</p>
    </footer>
  </div>
</template>
<style>
.app-container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

main {
  flex: 1; 
}
</style>