<script setup>
  const props = defineProps({
    isActive: {
      type: Boolean,
      required: false,
    },
  });
</script>

<template>
  <div :class="{ [$style.container]: true, [$style.visible]: props.isActive }">
    <div :class="$style.flex">
      <div :class="$style.header">
        <div :class="$style.list">
          <a href="" :class="{ [$style.link]: true, [$style.active]: true }"
            ><img
              src="/icons/chart-pie.png"
              alt=""
              :class="$style.icons"
            />Overview</a
          >
          <a href="" :class="{ [$style.link]: true, [$style.active]: false }"
            ><img
              src="/icons/document-report.png"
              alt=""
              :class="$style.icons"
            />Pages</a
          >
          <a href="" :class="{ [$style.link]: true, [$style.active]: false }"
            ><img
              src="/icons/shopping-bag.png"
              alt=""
              :class="$style.icons"
            />Sales</a
          >
          <a href="" :class="{ [$style.link]: true, [$style.active]: false }"
            ><img
              src="/icons/inbox-in.png"
              alt=""
              :class="$style.icons"
            />Messages</a
          >
          <a href="" :class="{ [$style.link]: true, [$style.active]: false }"
            ><img
              src="/icons/lock-closed.png"
              alt=""
              :class="$style.icons"
            />Authentication</a
          >
        </div>
        <div :class="$style.faq">
          <a href="" :class="{ [$style.link]: true, [$style.active]: false }"
            ><img
              src="/icons/clipboard-list.png"
              alt=""
              :class="$style.icons"
            />Docs</a
          >
          <a href="" :class="{ [$style.link]: true, [$style.active]: false }"
            ><img
              src="/icons/collection.png"
              alt=""
              :class="$style.icons"
            />Components</a
          >
          <a href="" :class="{ [$style.link]: true, [$style.active]: false }"
            ><img
              src="/icons/support.png"
              alt=""
              :class="$style.icons"
            />Help</a
          >
        </div>
      </div>
      <div :class="$style.footer">
        <a href="" :class="{ [$style.link]: true, [$style.active]: false }"
          ><img src="/icons/adjustments.png" alt="" :class="$style.icons"
        /></a>
        <a href="" :class="{ [$style.link]: true, [$style.active]: false }"
          ><img src="/icons/globe.png" alt="" :class="$style.icons"
        /></a>
        <a href="" :class="{ [$style.link]: true, [$style.active]: false }"
          ><img src="/icons/cog.png" alt="" :class="$style.icons"
        /></a>
      </div>
    </div>
  </div>
</template>

<style module lang="scss">
  .container {
    display: none;
    min-height: 100vh;
    height: 100%;
    background-color: #fff;

    @media (min-width: $tablet-size-land) {
      display: block;
      position: relative;
      width: 100%;
      border-right: 1px solid #e5e7eb;
    }
  }

  .visible {
    display: block;
    position: fixed;
    top: 71px;
    left: 0;
    width: 100vw;
  }

  .flex {
    display: flex;
    flex-flow: column wrap;
    justify-content: space-between;
    height: 100%;
    padding: 20px;
  }

  .list {
    border-bottom: 1px solid #e5e7eb;
  }

  .link {
    display: flex;
    align-items: center;
    color: var(--color-black);
    font-weight: 500;
    font-size: 16px;
    margin-bottom: 22px;
  }

  .active {
    color: var(--color-accent);
  }

  .icons {
    margin-right: 1rem;
  }

  .faq {
    padding: 20px 0;
  }

  .footer {
    display: flex;
    justify-content: center;
    gap: 22px;

    & > a {
      margin-bottom: 0;

      & > img {
        width: 24px;
        height: 24px;
        margin-right: 0;
      }
    }
  }
</style>
