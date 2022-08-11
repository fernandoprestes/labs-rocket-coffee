<script lang="ts" setup>
  import CardItem from './CardItem.vue';
</script>

<template>
  <ul>
    <CardItem
      title="SUCO DE LIMÃO"
      content="Lorem ipsum dolor site amet, adipsicing elit, sed diam nonummy nibh."
      :price="12.6"
    />
    <CardItem
      title="SUCO DE TAMARINDO"
      content="Lorem ipsum dolor site amet, adipsicing elit, sed diam nonummy nibh."
      :price="14.6"
    />
  </ul>
</template>
