<script setup lang="ts">
definePageMeta({
    layout: 'centered'
});

</script>

<template>
  <div class="prose">
    <h1>Inscription </h1>
    <form>
      <label>
        Nom et prénom
        <input type="text">
      </label>

      <label>
        Email
        <input type="email">
      </label>

      <label>
        Mot de passe
        <input type="password">
      </label>

      <label>
        Confirmation du mot de passe
        <input type="password">
      </label>
      <button type="button" class="btn">S'inscrire</button>
    </form>
    <p>
      Vous avez déjà un compte ?
      <NuxtLink class="uderline text-lime-600" to="/login">Se connecter !</NuxtLink>
    </p>
  </div>
</template>
