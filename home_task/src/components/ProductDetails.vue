<template>
    <div>
        <ProductVew :product="item" v-for="item in product" :id="item.id"/>
    </div>
</template>

<script>
import ProductVew from './productVew.vue';

    export default {
        data() {
        return {
            product:[{
                name:'phone1',
                price:12,
                available:true
            },
            {
                name:'phone2',
                price:10,
                available:false
            },
            {
                name:'phone3',
                price:16,
                available:true
            },
            ]
        };
    },
    components: {
    ProductVew
},
    
    }
</script>

<style scoped>

</style>