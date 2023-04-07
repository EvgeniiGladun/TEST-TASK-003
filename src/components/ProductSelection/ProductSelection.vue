<script>
export default {
    name: 'ProductSelection',
    data() {
        return {
            products: [],
            apiUrl: 'https://dev-su.eda1.ru/test_task/products.php'
        }
    },
    mounted() {
        this.getProducts()
    },
    methods: {
        async getProducts() {
            try {
                const response = await fetch(this.apiUrl)
                const data = await response.json()
                data.products.forEach((product) => {
                    this.products.push(product);
                });
            } catch (error) {
                console.error(error)
            }
        }
    }
}
</script>

<template>
    <section class="product-selection">
        <form class="selection-form">
            <div class="selection-form__wrapper">
                <label class="selection-form__label">Выберите продукцию</label>
                <select class="selection-form__select-item" name="select-item" id="select-form">
                    <option value="">Выбрать</option>
                    <option v-for="product in products" :key="product.id" :value="product.title">{{ product.title }}
                    </option>
                </select>
            </div>

            <div class="selection-form__wrapper">
                <label class="selection-form__label">Введите количество</label>
                <input class="selection-form__input" type="number" value="0">
            </div>
            <button class="selection-form__button">Добавить</button>
        </form>
    </section>
</template>

<style>
.product-selection {
    width: 100%;
    max-width: 394px;
}

.selection-form__wrapper {
    display: flex;
    flex-direction: column;
    margin-bottom: 37px;
}

.selection-form__wrapper:nth-child(2) {
    margin-bottom: 48px;
}

.selection-form__label {
    font-weight: 300;
    margin-bottom: 21px;
}

.selection-form__select-item {
    height: 54px;
    color: rgba(1, 112, 174, 1);
    padding: 12px 19px 12px 16px;
    border-bottom: 1px solid rgba(47, 166, 234, 1);
}

.selection-form__select-item:focus {
    outline: none;
}

.selection-form__input {
    border: none;
    font-weight: 300;
    font-size: 24px;
    line-height: 28px;
    padding: 12px 0 12px 16px;
    color: rgba(1, 112, 174, 1);
    border-bottom: 1px solid rgba(47, 166, 234, 1);
}

.selection-form__input:focus {
    outline: none;
}

.selection-form__button {
    width: 100%;
    height: 52px;
    font-size: 24px;
    line-height: 28px;
    border-radius: 4px;
    text-shadow: 0px 0px 1px rgba(0, 0, 0, 1);
    box-shadow: 0 4px 4px rgba(0, 0, 0, 0.25);
    color: rgba(255, 255, 255, 1);
    border: 1px solid rgba(0, 0, 0, 1);
    background-color: rgba(47, 166, 234, 1);
}
</style>
