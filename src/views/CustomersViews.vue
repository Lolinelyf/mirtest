<script setup>
  import { getCustomer } from '@/api/Customers';
  import CustomersComponent from '@/components/CustomersComponent.vue';
</script>

<template>
  <div :class="$style.container">
    <h1 class="title">Latest Customers</h1>
    <div :class="$style.flex">
      <CustomersComponent
        v-for="item in getCustomer()"
        :key="item.id"
        :name="item.name"
        :img="item.image"
        :mail="item.mail"
        :price="item.price"
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
