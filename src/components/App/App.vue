<script>
import MainPage from '../MainPage/MainPage.vue';
import HeaderItem from '../Header/HeaderItem.vue';
import FooterItem from '../Footer/FooterItem.vue';

export default {
  data() {
    return {
      city: '',
    };
  },
  components: {
    HeaderItem,
    MainPage,
    FooterItem,
  },
}

</script>

<template>
  <main class="main-conntent">
    <HeaderItem />
    <MainPage />
    <FooterItem />
  </main>
</template>

<style>
.main-conntent {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  max-width: 1440px;
  min-height: 100vh;
  margin: 0 auto;
}
</style>
