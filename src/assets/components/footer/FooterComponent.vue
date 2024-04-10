<template>
    <div>
        <FooterTop />
        <FooterMid />
        <FooterBottom />
    </div>
</template>

<script>
import FooterTop from './FooterTop.vue';
import FooterMid from './FooterMid.vue';
import FooterBottom from './FooterBottom.vue';


    export default {
        name: 'FooterComponent',
        components:{
            FooterTop,
            FooterMid,
            FooterBottom
        }
    }
</script>

<style lang="scss" scoped>

</style>