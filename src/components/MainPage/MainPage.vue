<script>
import ProductSelection from '../ProductSelection/ProductSelection.vue';
import itemProduct from '../ItemProduct/ItemProduct.vue';

export default {
    data() {
        return {};
    },
    components: {
        ProductSelection,
        itemProduct,
    },
}

</script>

<template>
    <section class="main-page">
        <ProductSelection />
        <itemProduct />
    </section>
</template>

<style>
.main-page {
    display: flex;
    margin: 0 26px;
}
</style>
