<script setup></script>

<template>
  <div :class="$style.container">
    <div :class="$style.flex">
      <h1 :class="$style.title">
        © 2021 Themesberg, LLC. All rights reserved.
      </h1>
      <div :class="$style.social">
        <a href="" :class="$style.item"
          ><img src="/icons/facebook-f.png" alt="" :class="$style.icon"
        /></a>
        <a href="" :class="$style.item"
          ><img src="/icons/twitter.png" alt="" :class="$style.icon"
        /></a>
        <a href="" :class="$style.item"
          ><img src="/icons/github.png" alt="" :class="$style.icon"
        /></a>
        <a href="" :class="$style.item"
          ><img src="/icons/dribbble.png" alt="" :class="$style.icon"
        /></a>
      </div>
    </div>
  </div>
</template>

<style module lang="scss">
  .container {
    width: 100%;
    background-color: #fff;
    border-radius: 1rem;
    margin-bottom: 1rem;
    padding: 48px 32px;
  }

  .flex {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: space-between;

    @media (min-width: $tablet-size-land) {
      flex-direction: row;
      align-items: center;
    }
  }

  .title {
    font-size: 16px;
    color: #6b7280;
    font-weight: 400;
    margin-bottom: 1rem;
    @media (min-width: $tablet-size-land) {
      margin-bottom: 0;
    }
  }
  .social {
    display: flex;
    gap: 24px;
  }

  .item {
    display: block;
    width: 24px;
    height: 24px;
  }
</style>
