<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <div class="header__logo">
      <img alt="Vue logo" class="logo" src="@/assets/img/fine-shop-logo.png" />
    </div>
    <div class="header__search">
      <input class="form-control" placeholder="search" />
    </div>
    <div class="header__actions">
      <ul>
        <li>
          <div class="account-iocn">
            <i class="fas fa-user"></i>
          </div>
        </li>
          <li>
          <div class="wishlist-iocn">
            <i class="fas fa-heart"></i>
          </div>
        </li>
          <li>
          <div class="cart-iocn">
            <i class="fas fa-cart-arrow-down"></i>
            <span class="cart-count">0</span>
          </div>
        </li>
         <li>
          <div class="cart-amount"></div>
        </li>
      </ul>


    </div>
    

    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style lang="scss">
@import '@/assets/scss/app.scss';

</style>
