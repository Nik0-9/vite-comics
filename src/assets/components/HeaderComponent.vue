<template>

    <header class="px-5">
        <div class="container d-flex justify-content-between align-items-center">
            <div>
                <img :src="logoHeader" alt="logo">
            </div>
            <div id="nav-header">
                <ul class="d-flex">
                    <li v-for="(item, index) in navHeader" :key="index">
                        <a :href="item.url" class="text-uppercase">
                            {{item.name}}
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'HeaderComponent',
    data() {
        return {
            logoHeader: '/img/dc-logo.png',
            navHeader: [
                {
                    name: 'characters',
                    url: '#'
                },
                {
                    name: 'comics',
                    url: '#'
                },
                {
                    name: 'movies',
                    url: '#'
                },
                {
                    name: 'tv',
                    url: '#'
                },
                {
                    name: 'games',
                    url: '#'
                },
                {
                    name: 'collectibles',
                    url: '#'
                },
                {
                    name: 'videos',
                    url: '#'
                },
                {
                    name: 'fans',
                    url: '#'
                },
                {
                    name: 'news',
                    url: '#'
                },
                {
                    name: 'shop',
                    url: '#'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

header {
    background-color: $backgroundHeader;
    padding: 10px;
    display: flex;
    ul{
        list-style: none;
    }
    li{
       margin: 0 10px; 
       font-size: 0.9rem;
       &:hover{
        border-bottom: 2px solid $backgroundFooterTop;
       }
    }
    a{
        color: black;
        text-decoration: none;
        &:hover{
        color: $backgroundFooterTop;
        }
    }
}
</style>