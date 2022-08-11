<script lang="ts" setup>
  import Logo from '../../components/Logo.vue';
  import Accordion from '../../components/Accordion.vue';
</script>

<template>
  <main class="o-container">
    <header class="header">
      <Logo />
      <p>Aberto todos os dias. 8h - 21h</p>
    </header>

    <Accordion class="accordion">
      <template #accordion-header> Brunch </template>
      <template #accordion-content>
        <div>
          <div class="card">
            <div class="card__text">
              <h4>Waffle Doce</h4>
              <p>Lorem ipsum dolor site amet, adipsicing elit, sed diam nonummy nibh.</p>
            </div>
            <div class="card__price">
              <span>R$ 37.70</span>
            </div>
          </div>
          <div class="card__content">
            <div class="card__text">
              <h4>Arroz Doce</h4>
              <p>Lorem ipsum dolor site amet, adipsicing elit, sed diam nonummy nibh.</p>
            </div>
            <div class="card__price">
              <span>R$ 37.70</span>
            </div>
          </div>
        </div>
      </template>
    </Accordion>
  </main>
</template>

<style lang="scss" scoped>
  .header {
    padding: 32px;
    color: var(--color-paragraph);
  }

  .accordion {
    font-family: var(--font-family-serif);
  }

  .card {
    display: flex;
    gap: 8px;
    margin-top: 16px;

    &__price {
      flex: 1 0 auto;
    }
  }
</style>
