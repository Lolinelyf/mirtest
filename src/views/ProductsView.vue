<script setup>
  import { getProduct } from '@/api/Products';
  import ProductComponent from '@/components/ProductComponent.vue';
</script>

<template>
  <div :class="$style.container">
    <h1 class="title">Top products</h1>
    <div :class="$style.flex">
      <ProductComponent
        v-for="item in getProduct()"
        :key="item.id"
        :name="item.name"
        :framework="item.framework"
        :size="item.size"
      />
    </div>
  </div>
</template>

<style module lang="scss">
  .container {
    width: 380px;
    background-color: #fff;
    border-radius: 1rem;
    margin-bottom: 1rem;
    padding: 24px;
  }
</style>
