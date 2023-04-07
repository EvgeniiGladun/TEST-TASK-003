<script>
export default {
    name: 'HeaderItem',
}
</script>

<template>
    <header class="header">
        <div class="header__wrapper">
            <h3 class="header__name">sf</h3>
        </div>
    </header>
</template>

<style>
.header__wrapper {
    background-color: rgba(117, 88, 88, 1);
    box-shadow: 0 4px 4px rgba(0, 0, 0, 0.25);
    height: 60px;
    margin: 0 auto;
}

.header__name {
    color: rgba(255, 255, 255, 1);
    padding: 16px 0 16px 26px;
}
</style>
