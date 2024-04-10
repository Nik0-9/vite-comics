<template>
    <footer id="footer-top">
        <div class="container d-flex justify-content-between align-items-center">
            <div v-for="(item, index) in navFooterTop" :key="index">
                <img :src="item.icon" alt="icona">
                <a href="#" class="text-uppercase">{{item.text}}</a>
            </div>
        </div>
    </footer>
</template>

<script>
    export default {
        name: 'FooterTop',
        data(){
            return{
                navFooterTop: [
                    {
                        icon: '/img/buy-comics-digital-comics.png',
                        text: 'digital-comics',
                        url: '#'
                    },
                    {
                        icon: '/img/buy-comics-merchandise.png',
                        text: 'dc merchandise',
                        url: '#'
                    },
                    {
                        icon: '/img/buy-comics-subscriptions.png',
                        text: 'subscription',
                        url: '#'
                    },
                    {
                        icon: '/img/buy-comics-shop-locator.png',
                        text: 'comic shop locater',
                        url: '#'
                    },
                    {
                        icon: '/img/buy-dc-power-visa.svg',
                        text: 'dc power visa',
                        url: '#'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../../styles/partials/variables' as *;
#footer-top{
    background-color: $backgroundFooterTop;
    padding: 40px 0;
    img{
        width: 40px;
    }
    a{
        color: white;
        text-decoration: none;
    }
}


</style>