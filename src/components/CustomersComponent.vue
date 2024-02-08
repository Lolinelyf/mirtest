<script setup>
  const props = defineProps({
    name: {
      type: String,
      required: true,
    },
    img: {
      type: String,
      required: true,
    },
    mail: {
      type: String,
      required: true,
    },
    price: {
      type: String,
      required: true,
    },
  });
</script>

<template>
  <div :class="$style.card">
    <div :class="$style.person">
      <img :src="props.img" alt="" :class="$style.img" />
      <div :class="$style.info">
        <h2 :class="$style.name">{{ props.name }}</h2>
        <p :class="$style.mail">{{ props.mail }}</p>
      </div>
    </div>

    <p :class="$style.price">{{ props.price }}</p>
  </div>
</template>

<style module lang="scss">
  .card {
    display: flex;
    flex-flow: row nowrap;
    align-items: center;
    justify-content: space-between;
    height: 59px;
    width: 100%;

    &:not(:last-child) {
      border-bottom: 1px solid #e5e7eb;
    }
  }
  .person {
    display: flex;
    align-items: center;
  }
  .img {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    overflow: hidden;
    margin-right: 8px;
  }

  .info {
    display: flex;
    flex-flow: column wrap;
  }

  .name {
    font-size: 16px;
    font-weight: 600;
    color: var(--color-black);
    margin-bottom: 0;
  }

  .mail {
    font-size: 12px;
    color: var(--color-grey);
    margin-bottom: 0;
  }
  .price {
    font-size: 16px;
    font-weight: 600;
    color: var(--color-black);
    margin-bottom: 0;
  }
</style>
