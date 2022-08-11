<script lang="ts" setup>
  import CardItem from './CardItem.vue';
</script>

<template>
  <ul>
    <CardItem
      title="WAFFLE DOCE"
      content="Lorem ipsum dolor site amet, adipsicing elit, sed diam nonummy nibh."
      :price="17.5"
    />
    <CardItem
      title="ARROZ DOCE"
      content="Lorem ipsum dolor site amet, adipsicing elit, sed diam nonummy nibh."
      :price="16.89"
    />
    <CardItem
      title="MAÇA VERDE DOCE"
      content="Lorem ipsum dolor site amet, adipsicing elit, sed diam nonummy nibh."
      :price="23.89"
    />
  </ul>
</template>
