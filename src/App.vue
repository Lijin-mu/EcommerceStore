<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <div class="container">
      <div class="header">
        <div class="header__logo">
          <img alt="Vue logo" class="logo" src="@/assets/img/fine-shop-logo.png" />
        </div>
        <div class="header__search">
          <input class="form-control" placeholder="search" />
        </div>
        <div class="header__actions">
          <ul>
            <li>
              <div class="header-action account-icon">
                <font-awesome-icon icon="fa-solid fa-user" />
              </div>
            </li>
            <li>
              <div class="header-action wishlist-icon">
                <font-awesome-icon icon="fa-solid fa-heart" />
              </div>
            </li>
            <li>
              <div class="header-action cart-icon">
                <font-awesome-icon icon="fa-solid fa-cart-shopping" />
                <span class="cart-count">0</span>
                <span class="cart-amount">12.00</span>
              </div>
            </li>
          </ul>

        </div>
      </div>
      <div class="navigation">
         <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
    </nav>
      </div>
    </div>


  </header>
  <RouterView />
  <footer>
    &copy 2hts
  </footer>
</template>

<style lang="scss">
@import '@/assets/scss/app.scss';
#app{
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 100vh;

}
</style>
