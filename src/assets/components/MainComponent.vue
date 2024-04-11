<template>
    <div id="jumbo">
    </div>
    <main>
        <div class="container p-4">
            <div class="series d-flex justify-content-center align-items-center">
                <h3 class="text-uppercase">
                    current series
                </h3>
            </div>
            <div class="row ">
                <div class="col-12 col-md-4 col-lg-3 col-xl-2 text-light mb-3" v-for="(item, index) in comics" :key="index">
                    <CardComponent :image="item.thumb" :title="item.series" :type="item.type" :price="item.price" />
                </div>
            </div>
            <div class="text-center">
                <span class="text-uppercase load-more">load more</span>
            </div>
        </div>
    </main>
</template>

<script>
import CardComponent from './CardComponent.vue';
import { comics } from '../../../src/data/store.js';
export default {
    name: 'MainComponent',
    components: {
        CardComponent
    },
    data() {
        return {
            comics,
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

#jumbo {
    background-image: url('/img/jumbotron.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    height: 350px;
    width: 100%;
}
h3{
    margin: 0;
    padding: 0;
}

.series{
    width: 250px;
    background-color: $backgroundFooterTop;
    transform: translateY(-120%);
}

main {
    background-color: $backgroundMain;
    color: white;
    font-size: 3rem;
}
.load-more{
    margin: 0 auto;
    font-size: 1.5rem;
    padding: 6px 10px;
    background-color: $backgroundFooterTop;
}

</style>