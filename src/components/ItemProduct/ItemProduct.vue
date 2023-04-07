<script>
export default {
    name: 'ItemProduct',
}
</script>

<template>
    <section class="items-product">
        <div class="product">
            <label class="product__label">Название товара</label>
            <label class="product__label">Количество</label>
            <label class="product__label">Стоимость</label>
            <p class="product__name">Борщевой набор номер три </p>
            <p class="product__quantity product__position">11 шт.</p>
            <p class="product__price product__position">1100.00</p>
        </div>
    </section>
</template>

<style>
.items-product {
    padding: 0 50px;
}

.product {
    display: grid;
    grid-template-columns: 5fr 1fr 1fr;
    gap: 20px 49px;
}

.product__label {
    font-weight: 300;
    color: rgba(1, 112, 174, 1);
}

.product__name,
.product__quantity,
.product__price {
    font-weight: 300;
}

.product__position {
    display: flex;
    justify-content: end;
}
</style>
