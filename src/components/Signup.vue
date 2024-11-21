<script setup>
</script>

<template>
  <div class="container-center">
    <header>
    </header>
    <div class="card p-4 shadow-lg">
      <form>
        <div class="mb-3">
          <input type="email" class="form-control bg-dark text-white" id="bejemail" placeholder="Email cím megadása" />
        </div>
        <div class="mb-3">
          <input type="password" class="form-control bg-dark text-white" id="bejpass" placeholder="Jelszó megadása" />
        </div>
        <div class="form-check mb-3">
          <input class="form-check-input" type="checkbox" id="notrobot" />
          <label class="form-check-label text-white" for="notrobot">Nem vagyok robot</label>
        </div>
        <button type="submit" class="btn btn-primary w-100">Bejelentkezés</button>
      </form>
    </div>
  </div>
</template>

<style scoped>
form {
  display: flex;
  flex-direction: column;
  gap: 10px;
  align-items: center;
}

.card {
  max-width: 400px;
  width: 100%;
  background-color: #1e1e2f;
  border-radius: 15px;
}

.container-center {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-size: cover;
  background-position: center;
}
</style>
