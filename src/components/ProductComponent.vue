<script setup>
  const props = defineProps({
    name: {
      type: String,
      required: true,
    },
    framework: {
      type: String,
      required: true,
    },
    size: {
      type: Number,
      required: true,
    },
  });
</script>

<template>
  <div :class="$style.card">
    <div :class="$style.info">
      <h2 :class="$style.name">{{ props.name }}</h2>
      <p :class="$style.framework">{{ props.framework }}</p>
    </div>

    <p :class="$style.price">
      <strong>{{ props.size }}</strong> sales
    </p>
  </div>
</template>

<style module lang="scss">
  .card {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 59px;

    &:not(:last-child) {
      border-bottom: 1px solid #e5e7eb;
    }
  }

  .name {
    font-size: 16px;
    font-weight: 600;
    color: var(--color-black);
    margin-bottom: 0;
  }

  .framework {
    font-size: 12px;
    color: var(--color-grey);
    margin-bottom: 0;
  }

  .price {
    font-size: 16px;
    font-weight: 400;
    margin-bottom: 0;
  }
</style>
