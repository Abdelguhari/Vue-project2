<script>
    import axios from "axios"
    import { RouterLink } from "vue-router"

    export default {
        data() {
            return {
                products: []
            }
        },
        methods: {
            getData() {
                axios.get('https://fakestoreapi.com/products')
                    .then(response => {
                        this.products = response.data
                    })
                    .catch(error => {
                        console.log(error)
                    })
            },
            getLink(product){
                return `/products/${product.id}`
            }
        },
        mounted() {
            this.getData()
        }
    }
</script>

<template>
    <div class="grid grid-cols-2 place-items-center mx-[20px] gap-[50px] my-[30px]">
        <div class="flex flex-col items-center gap-[10px] p-[15px] border border-slate-300 rounded-lg bg-slate-200" v-for="product in products" :key="product.id">
            <h2>{{ product.title }}</h2>
            <div class="w-[200px]">
                <img :src="product.image" class="w-100" alt="">
            </div>
            <p> price: {{ product.price }} USD</p>
            <RouterLink class="py-[5px] px-[20px] bg-blue-300 hover:bg-blue-200 rounded transition" :to="getLink(product)">View</RouterLink>
        </div>
    </div>
</template>
