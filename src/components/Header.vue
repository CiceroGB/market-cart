<template>
  <nav>
    <router-link to="/" class="logo">
      <img src="@/assets/ranek.svg" alt="Ranek" />
    </router-link>
    <router-link to="/login" class="btn"> Vender / Login </router-link>
  </nav>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style>
</style>