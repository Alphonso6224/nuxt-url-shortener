<script setup lang="ts">
definePageMeta({
    layout: 'centered'
});

</script>

<template>
  <div class="prose">
    <h1>Connexion</h1>
    <form>
      <label>
        Email
        <input type="email">
      </label>

      <label>
        Mot de passe
        <input type="password">
      </label>
      <button type="button" class="btn">Se connecter</button>
    </form>
    <p>
      Pas de compte ?
      <NuxtLink class="uderline text-lime-600" to="/register">inscrivez-vous !</NuxtLink>
    </p>
  </div>
</template>
