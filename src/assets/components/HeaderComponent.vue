<template>

    <header>
        <div class="container d-flex justify-content-between align-items-center">
            <div>
                <img :src="logoHeader" alt="logo" class="w-75 p-2">
            </div>
            <div id="nav-header">
                <ul class="d-flex">
                    <li v-for="(item, index) in navHeader" :key="index">
                        <a :href="item.url" class="text-uppercase after">
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

    ul {
        list-style: none;
        margin: 0;
        padding: 0;
        display: flex;
        gap: 20px; 
    }

    li {
        font-size: 0.9rem;
    }

    a {
        color: black;
        font-weight: 500;
        text-decoration: none;
        position: relative; 
    }

    a::after {
        content: "";
        position: absolute;
        left: 0;
        top: 61px;
        width: 100%;
        height: 3px;
        background-color: $backgroundFooterTop;
        visibility: hidden; 
        transform: scaleX(0);
        
    }

    a:hover::after {
        visibility: visible; 
        transform: scaleX(1);
    }
}
</style>