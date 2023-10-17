<template>
    <div class="card">
        <h3>{{ product.name }}</h3>
        <p> Цена {{ formattedPrice }}</p>
        <p v-if="product.available">Available</p>        
        <p v-else>Out of stock</p>
    </div>
</template>

<script>
    export default {
        props:{
            product:Object,
        },
        computed:{
        formattedPrice(){
            return `$ ${this.product.price}`
        }
    }
    }
</script>

<style scoped>
    .card{
        width: 350px;
        height: inherit;
        margin: 10px;
    background: #fff;
    font-family: Montserrat, sans-serif;;
    font-size: 24px;
    line-height: 30px;
    font-weight: bold;
    color: #009688;
    padding: 40px;
    box-shadow:
	inset #009688 0 0 0 5px, 
    inset #059c8e 0 0 0 1px, 
    inset #2613d3 0 0 0 10px, 
    inset #1fbdae 0 0 0 11px, 
    inset #8ce9ff 0 0 0 16px, 
    inset #48e4d6 0 0 0 17px, 
    inset #e5f9f7 0 0 0 21px, 
    inset #bfecf7 0 0 0 22px;
  text-shadow: 3px 3px 1px #bfecf7;
    }
</style>