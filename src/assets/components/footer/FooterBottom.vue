<template>
    <div id="footer-bottom">
        <div class="container d-flex justify-content-between align-items-center p-4">
            <button class="text-uppercase py-2 px-3">sign-up now!</button>
            <div>
                <span id="follow" class="text-uppercase">follow us</span>
                <span v-for="(icon, index) in socialIcon">
                <img :src="icon" alt="icon" class="m-3">
                </span>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'FooterBottom',
        data(){
            return{
                socialIcon:[
                    '/img/footer-facebook.png',
                    '/img/footer-pinterest.png',
                    '/img/footer-twitter.png',
                    '/img/footer-youtube.png',
                    '/img/footer-periscope.png',
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../../styles/partials/variables' as *;

#footer-bottom{
    background-color: $backgroundFooterBottom;
}
button{
    background: transparent;
    color: white;
    border: 3px solid $backgroundFooterTop;
}
#follow{
color: $backgroundFooterTop;
font-size: 1.3rem;
font-weight: 700;
}

</style>