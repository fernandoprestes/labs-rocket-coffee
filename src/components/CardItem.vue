<script lang="ts" setup>
  interface PropsCardItem {
    title: string;
    content: string;
    price: number;
  }
  defineProps<PropsCardItem>();

  function formatterCurrency(value: number) {
    const formatter = new Intl.NumberFormat('pt-BR', {
      style: 'currency',
      currency: 'BRL',
      minimumFractionDigits: 2,
    });
    return formatter.format(value);
  }
</script>

<template>
  <li class="card">
    <div>
      <h4>{{ title }}</h4>
      <p>{{ content }}</p>
    </div>
    <div class="card__price">
      <span>{{ formatterCurrency(price) }}</span>
    </div>
  </li>
</template>
<style lang="scss" scoped>
  .card {
    display: flex;
    gap: 8px;
    margin-top: 16px;

    p {
      color: var(--color-paragraph);
    }

    &__price {
      flex: 1 0 auto;
    }
  }
</style>
