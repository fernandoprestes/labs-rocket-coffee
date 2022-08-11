<script setup lang="ts">
  import { computed, reactive, ref } from 'vue';

  export interface AccordionType {
    count: number;
    active: number | null;
  }

  const Accordion: AccordionType = reactive({
    count: 0,
    active: null,
  });

  const index = ref(Accordion.count++);

  const isVisible = computed(() => {
    return index.value === Accordion?.active;
  });

  function open() {
    if (isVisible.value) {
      Accordion.active = null;
      return;
    }
    Accordion.active = index.value;
  }

  function start(el: HTMLDivElement) {
    console.log(typeof el);
    el.style.height = el.scrollHeight + 'px';
  }

  function end(el: HTMLDivElement) {
    el.style.height = '';
  }
</script>

<template>
  <div>
    <button
      class="accordion-button"
      @click="open"
    >
      <slot name="accordion-header"></slot>
    </button>

    <transition
      name="accordion"
      @enter="start"
      @after-enter="end"
      @before-leave="start"
      @after-leave="end"
    >
      <div v-if="isVisible">
        <slot name="accordion-content"></slot>
      </div>
    </transition>
  </div>
</template>

<style lang="scss" scoped>
  .accordion-enter-active,
  .accordion-leave-active {
    overflow: hidden;
    transition: height 0.3s ease, opacity 0.3s ease;
    will-change: height, opacity;
  }

  .accordion-enter-from,
  .accordion-leave-to {
    height: 0 !important;
    opacity: 0;
  }

  .accordion-button {
    width: 100%;
    padding: 8px;
    margin-top: 8px;
    font-size: var(--font-size-xl);
    font-weight: 700;
    text-align: center;
    cursor: pointer;
    background: var(--color-card-header);
  }
</style>
