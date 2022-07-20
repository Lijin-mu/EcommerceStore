<template>
<div class="product">
    <div class="product-image">
    <img :src="image" />
    </div>
    <div class="product-details">
       <div class="product-details__title">{{ title }}</div>
         <div class="product-details__rating"></div>
        <div class="product-details__description">{{ description }}</div>
        <div class="product-details__price">$ {{ price }}</div>
        <div class="product-details__actions">
            <div class="add-to-cart"></div>
            <div class="add-to-wishlist"></div>
        </div>
    </div>
</div>

</template>

<script>
export default {
  name: 'ProductBox',
 
  data () {
    return {
  
    }
  },
  props: {
    title: String,
    description: String,
    price: Number,
    image: String
  },
  computed: {

  },
  mounted () {

  },
  methods: {

  }
}
</script>

<style lang="scss">

.product{
    width: 100%;
    max-width: 250px;
    height: auto;
    padding: 15px;
    border: 1px solid #ccc;
    &-image{
        width:100%;
        height: 250px;
        img{
            width: 100%;
            height: 250px;
            object-fit: contain;
            object-position: center;
        }
    }
    &-details{
        width: 100%;
        height: auto;
        margin-top: 20px;
        &__title{
          width: 100%;
          font-size: 20px;
          color: #000;
          font-weight: bold;
          line-height: 26px;
          display: -webkit-box;
          max-width: 100%;
          -webkit-line-clamp: 2;
          -webkit-box-orient: vertical;
          overflow: hidden;
          height: 52px;
        }
        &__description{
          margin-top: 15px;
          font-size: 16px;
          line-height: 24px;
          display: -webkit-box;
          max-width: 100%;
          -webkit-line-clamp: 4;
          -webkit-box-orient: vertical;
          overflow: hidden;
          height: 96px;
        }
        &__price {
            font-size: 18px;
            color: #000;
            font-weight: bold;
        }
    }
}

</style>