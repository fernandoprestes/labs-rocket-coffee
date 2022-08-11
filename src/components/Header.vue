<script lang="ts" setup>
  import Logo from './Logo.vue';
</script>

<template>
  <header class="header">
    <Logo />
    <p>Aberto todos os dias. 8h - 21h</p>
  </header>
</template>
<style lang="scss" scoped>
  .header {
    padding: 32px;
    color: var(--color-paragraph);
  }
</style>
