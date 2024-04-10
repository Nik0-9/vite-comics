<template>
    <HeaderComponent />
    <MainComponent />
    <FooterComponent />
</template>

<script>
import HeaderComponent from './assets/components/HeaderComponent.vue';
import MainComponent from './assets/components/MainComponent.vue';
import FooterComponent from './assets/components/footer/FooterComponent.vue';

  export default {
    name: 'App',
    components:{
        HeaderComponent,
        MainComponent,
        FooterComponent
    }
  }
</script>

<style lang="scss" scoped>

</style>