<script setup></script>

<template>
  <header :class="$style.header">
    <div class="container">
      <div :class="$style.flex">
        <div :class="$style.left">
          <a href="" :class="$style.logo"><img src="/logo.png" alt="" /></a>
          <form action="" :class="$style.form">
            <button :class="$style.button"></button>
            <input
              type="search"
              id="site-search"
              name="q"
              placeholder="Search"
              :class="$style.search"
            />
          </form>
          <slot></slot>
        </div>
        <div :class="$style.person">
          <a href="" :class="$style.notification"
            ><img src="/icons/bell.png" alt="bell" :class="$style.icon"
          /></a>
          <a href="" :class="$style.avatar"
            ><img src="/img/Avatar-6.png" alt="avatar" :class="$style.img"
          /></a>
        </div>
      </div>
    </div>
  </header>
</template>

<style module lang="scss">
  .header {
    background-color: #fff;
    border-bottom: 1px solid #e5e7eb;
  }

  .flex {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 70px;
  }

  .left {
    display: flex;
    align-items: center;
  }

  .logo {
    display: none;
    @media (min-width: $tablet-size-land) {
      display: block;
      width: 35px;
      height: 35px;
      margin-right: 2rem;
    }
  }

  .form {
    display: none;
    @media (min-width: $tablet-size-land) {
      display: flex;
      width: 400px;
      height: 43px;
      background-color: #f9fafb;
      border-radius: 1rem;
      border: 1px solid #e5e7eb;
    }
  }

  .button {
    width: 45px;
    height: 45px;
    background-color: initial;
    background-image: url('/icons/search.png');
    background-position: center;
    background-repeat: no-repeat;
  }

  .search {
    width: 100%;
    border-radius: 0 16px 16px 0;
    border: none;
    background-color: initial;
    font-size: 16px;
    &:focus-visible {
      outline: none;
    }
  }

  .person {
    display: flex;
    align-items: center;
  }

  .notification {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-right: 12px;
  }

  .img {
    display: block;
    width: 32px;
    height: 32px;
    border-radius: 50%;
    overflow: hidden;
  }
</style>
