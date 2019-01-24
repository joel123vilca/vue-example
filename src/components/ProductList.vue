<template>
     <div>
         <h1>List Products</h1>
         <ul>
             <li v-for="product in products" :key="product.id"> {{product.title}}.{{product.price}}
             </li>
         </ul>
     </div>
</template>

<script>
import shop from '@/api/shop.js';
import store from '@/store/index.js';
export default {
    computed: {
        products () {
            return store.state.products
        }
    },
    created () {
        shop.getProducts(products => {
            store.commit('setProducts', products)
        })
    }
}
</script>

<style scoped>

</style>
