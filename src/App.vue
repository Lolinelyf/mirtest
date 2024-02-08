<script setup>
  import { ref } from 'vue';

  import HeaderViews from '@/views/HeaderViews.vue';
  import NavigationViews from '@/views/NavigationViews.vue';
  import SalesViews from '@/views/SalesViews.vue';
  import CustomersViews from '@/views/CustomersViews.vue';
  import ProductsView from '@/views/ProductsView.vue';
  import TransactionsViews from '@/views/TransactionsViews.vue';
  import FooterViews from '@/views/FooterViews.vue';

  const visibleMenu = ref(false);

  function openMenu() {
    visibleMenu.value = !visibleMenu.value;
    document.documentElement.classList.toggle('overflow');
  }
</script>

<template>
  <HeaderViews @click="openMenu" />

  <div :class="$style.grid">
    <NavigationViews :isActive="visibleMenu" />

    <div :class="$style.content">
      <main :class="$style.main">
        <SalesViews />
        <div :class="$style.flex">
          <CustomersViews :class="$style.customers" />
          <ProductsView :class="$style.products" />
        </div>
        <TransactionsViews :class="$style.transactions" />
      </main>
      <FooterViews />
    </div>
  </div>
</template>

<style module lang="scss">
  .grid {
    display: grid;
    grid-template-columns: 1fr;
    width: 100%;
    max-width: 1600px;
    margin-right: auto;
    margin-left: auto;

    @media (min-width: $tablet-size-land) {
      grid-template-columns: 250px 1fr;
    }
  }

  .content {
    width: 100vw;
    padding: 1rem 1rem 0 1rem;
    @media (min-width: $tablet-size-land) {
      width: 100%;
    }
  }
  .main {
    width: 100%;
  }
  .flex {
    display: flex;
    flex-direction: column;
    width: 100%;
    @media (min-width: $tablet-size-land) {
      flex-direction: row;
    }
  }

  .customers {
    width: 100%;

    @media (min-width: $tablet-size-land) {
      flex: 0 0 380px;
      width: 380px;
      margin-right: 1rem;
    }
  }
  .products {
    width: 100%;
    @media (min-width: $tablet-size-land) {
      flex: 0 0 calc(100% - (380px + 16px));
      width: calc(100% - (380px + 16px));
    }
  }
</style>
