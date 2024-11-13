<script setup>

</script>

<template>
  <header>
    <img src="/src/assets/result.png" alt="GatheringGalaxy" title="Gathering Galaxy">
    GatheringGalaxy
  </header>
  <main>
    <form>
      <input type="text" id="bejemail" placeholder="Email cím megadása">
      <input type="password" id="bejpass" placeholder="Jelszó megadása">
      <button id="bejgomb">Bejelentkezés</button>
    </form>
    <a href="">Nincs fiókod? Regisztrálj!</a>
    <div class="Registration">
      <form>
        <input type="text" id="regname" placeholder="Felhasználói név">
        <input type="text" id="regemail" placeholder="Email cím">
        <input type="password" id="regpass" placeholder="Jelszó">
        <input type="password" id="regrepass" placeholder="Jelszó megerősítése">
        <button id="bejgomb">Bejelentkezés</button>
      </form>
      <a href="">Van már fiokód? Jelentkezz be!</a>
    </div>
  </main>
  <footer>
    Copyright
  </footer>
</template>

<style scoped></style>
