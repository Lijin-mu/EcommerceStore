<template>
<div class="container">
 <div class="shop">
    <div class="products-list">
      <div v-for="product in products" class="products-list__item">
          <ProductBox :image="product.image" :title="product.title" :description="product.description" :price="product.price" />
      </div>
      
    </div>

  </div>
</div>
 
</template>

<script>

import ProductBox from '../../ProductBox/index.vue';

  const API_URL = `https://fakestoreapi.com/`

export default {
  name: 'ShopView',


   data: () => ({
    fetchItem: 'products',
    products: null
  }),

    created() {
    // fetch on init
    this.fetchData()
  },

    methods: {
    async fetchData() {
      const url = `${API_URL}${this.fetchItem}`
      this.products = await (await fetch(url)).json()
    },

  },

  components: {
    ProductBox
  },
    
}
</script>



<style lang="scss"> 
.shop {
    padding: 50px 0;
}
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
  .products-list{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: flex-start;
    width: auto;
    margin-left: -5px;
    margin-right: -5px;
    &__item{
    width: 20%;
    padding: 5px;
    }
  }

}
</style>