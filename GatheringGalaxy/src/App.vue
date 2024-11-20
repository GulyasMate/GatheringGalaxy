<script setup>

</script>

<template>
  <header>
    <img src="/src/assets/result.png" alt="GatheringGalaxy" title="Gathering Galaxy">
    <h1>GatheringGalaxy</h1>
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

<style scoped>
header {
  background-color: #44165A;
  color: #DFD1EB;
  margin: -10px;
  filter: drop-shadow(0, 4, 4, black)
}

input {
  border-radius: 20px;
  margin-top: 20px;
  padding: 10px 20px;
  background-color: #B39BCD;
  color: #DFD1EB;
}

input:focus {
  background-color: #DFD1EB;
  color: #B39BCD;
}

button {
  border-radius: 6px;
  background-color: #5E3674;
  color: #DFD1EB;
  margin-top: 20px;
  padding: 10px 20px;
}

button:hover {
  border-radius: 6px;
  background-color: #DFD1EB;
  color: #5E3674;
  margin-top: 20px;
  padding: 10px 20px;
}

a {
  text-decoration: none;
  color: #DFD1EB;
}

a:hover {
  color: #5E3674;
}

form {
  background-color: #1E3768;
  border-radius: 10px;
}

footer {
  background-color: #5F207D;
  color: #DFD1EB;
  margin: -10px;
  filter: drop-shadow(0, 4, 4, black);
  text-align: center;
}
</style>
