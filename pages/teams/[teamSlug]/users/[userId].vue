<script setup>
const route = useRoute();
const message = computed(
  () =>
    `I'm on team ${route.params.teamSlug} and my user id ${route.params.userId}`
);
</script>
<template>
  <p>
    {{ message }}
  </p>
</template>
