<template>
    <div>
        <h1 class="text-3xl text-red-500">Product Id : {{ product.id }} </h1>
        <p>{{ product.title }}</p>
    </div>
</template>

<script setup>
const uri = 'https://fakestoreapi.com/products/';
const { id } = useRoute().params;

const { data: product } = await useFetch(uri + id);

console.log();

</script>

<style lang="scss" scoped></style>