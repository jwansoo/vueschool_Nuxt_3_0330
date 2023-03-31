<script lang="ts" setup>
const user = useUser();
</script>

<template>
  <div>
    <div>
      <nav style="display: flex; gap: 10px">
        <nuxt-link to="/">Home</nuxt-link> |
        <nuxt-link to="/movies">Movies</nuxt-link> |
        <nuxt-link to="https://vueschool.io">vue school</nuxt-link>
        <nuxt-link v-if="!user.isLoggedIn" to="/login">Login</nuxt-link>
        <a href="#" v-else @click.prevent="user.isLoggedIn = false">Logout</a>
        Test
      </nav>
      <slot></slot>
    </div>
  </div>
  s
</template>

<style scoped></style>
