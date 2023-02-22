<script>
import Product from './Product.vue';

export default{
    components:{
        Product
    },
    data() {
        return{
            //
            // username: 'Cliff',
            // category: 'Books'
            // products:[
            //     {
            //         id: '1',
            //         name: 'airpods'
            //     },
            //     {
            //         id: '2',
            //         name: 'kindle'
            //     },
            //     {
            //         id: '3',
            //         name: 'keyboard'
            //     }
            // ]
            // isValid: true

            products:[
                {
                    id: '1',
                    imageUrl: "http://loremflickr.com/150/150?random=1",
                    productName: "Product 1",
                    releaseDate: "May 31, 2020",
                    description: "Lorem ipsum dolor sit amet, consecteur...",
                    rating: 4
                },
                {
                    id: '2',
                    imageUrl: "http://loremflickr.com/150/150?random=2",
                    productName: "Product 1",
                    releaseDate: "October 31, 2017",
                    description: "Lorem ipsum dolor sit amet, consecteur...",
                    rating: 2
                },
                {
                    id: '3',
                    imageUrl: "http://loremflickr.com/150/150?random=3",
                    productName: "Product 1",
                    releaseDate: "July 30, 2022",
                    description: "Lorem ipsum dolor sit amet, consecteur...",
                    rating: 5
                }
            ]
        }
    }

}
</script>
<template>
    <div>
        <!-- <h1>Products: {{ username }} by {{ category }}</h1>
        <h1>{{ category + ' by ' + username }}</h1>
        <h1>{{ username ? username : 'no username' }}</h1> -->
    </div>
    <div v-for="product in products" :key="product.id">
        <!-- <h3>{{ product.id }}: {{ product.name }}</h3> -->
        <Product :data="product" />
    </div>
    <!-- <button type="button" class="btn btn-primary">Primary</button>
    <button type="button" class="btn btn-danger" v-bind:disabled="!isValid">Danger</button> -->
</template>