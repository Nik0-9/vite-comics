<template>
    <div id="footer-mid">
        <div class="container d-flex justify-content-between">
            <div id="left">
                <div class="d-flex mt-5">
                    <ul v-for="(item, index) in footerList" :key="index" >
                        <h4>{{item.title}}</h4>
                        <li v-for="(listitem, i) in item.list" :key="i">
                        <a href="#">{{listitem}}</a>
                    </li>
                    </ul>
                </div>
            </div>
            <div id="right">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterMid',
    data() {
        return {
            footerList: [
                {
                    title: 'DC COMICS',
                    list: [
                        'Characters',
                        'Comics',
                        'Movies',
                        'TV',
                        'Games',
                        'Videos',
                        'News'
                    ]
                },
                {
                    title: 'SHOP',
                    list: [
                        'Shop DC',
                        'Shop DC Collectibles'
                    ]
                },
                {
                    title: 'DC',
                    list: [
                        'Terms Of Use',
                        'Privacy policy (New)',
                        'Ad Choices',
                        'Advertising',
                        'Jobs',
                        'Subscriptions',
                        'Talent Workshops',
                        'CPSC Certificates',
                        'Ratings',
                        'Shop Help',
                        'Contact Us'
                    ]
                },
                {
                    title: 'SITES',
                    list: [
                        'DC',
                        'MAD Magazine',
                        'DC Kids',
                        'DC Universe',
                        'DC Power Visa'
                    ]
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../../styles/partials/variables' as *;

#footer-mid {
    background-image: url('/img/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    ul{
        color: white;
        list-style: none;
    }
    a{
        text-decoration: none;
        color: rgb(180, 180, 180);
    }

    #right{
        width: 100%;
        background-image: url('/img/dc-logo-bg.png');
        background-repeat: no-repeat;
        background-position: center;
    }
}
</style>