<script setup>
import { ref } from 'vue';
import Registration from './components/Registration.vue';
import Signup from './components/Signup.vue';

const currentView = ref('home');

const setView = (view) => {
  currentView.value = view;
};
</script>
<template>
  <div class="app-container">
    <header>
      <img src="/src/assets/result.png" alt="GatheringGalaxy" title="Gathering Galaxy">
      <h1>GatheringGalaxy</h1>
    </header>
    <main>
      <div v-if="currentView === 'home'">
        <button @click="setView('registration')">Regisztráció</button>
        <button @click="setView('signup')">Bejelentkezés</button>
      </div>
      <div v-if="currentView === 'registration'">
        <Registration />
        <button @click="setView('home')">Vissza a főoldalra</button>
      </div>
      <div v-if="currentView === 'signup'">
        <Signup />
        <button @click="setView('home')">Vissza a főoldalra</button>
      </div>
    </main>
    <footer>
      &copy Copyright
    </footer>
  </div>
</template>

<style scoped>
.app-container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

main {
  flex: 1; 
}
</style>