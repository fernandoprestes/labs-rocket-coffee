<script lang="ts" setup>
  import Accordion from '~/components/Accordion.vue';
  import Header from '../../components/Header.vue';
  import CardListBranch from '../../components/CardListBranch.vue';
  import CardListDrink from '../../components/CardListDrink.vue';
</script>

<template>
  <main class="o-container">
    <Header />
    <Accordion class="accordion">
      <template #accordion-header> BRUNCH </template>
      <template #accordion-content>
        <CardListBranch />
      </template>
    </Accordion>
    <Accordion class="accordion">
      <template #accordion-header> DRINKS </template>
      <template #accordion-content>
        <CardListDrink />
      </template>
    </Accordion>
  </main>
</template>

<style lang="scss" scoped>
  .accordion {
    font-family: var(--font-family-serif);
  }
</style>
