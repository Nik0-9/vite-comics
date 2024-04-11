<template>
    <div id="jumbo">np
    </div>
    <main>
        <div class="container p-4">
            <div class="series">
                <h3 class="text-uppercase ">current series</h3>
            </div>
            <div class="row">
                <div class="col-12 col-md-4 col-lg-3 col-xl-2 text-light " v-for="(item, index) in comics" :key="index">
                    <CardComponent :image="item.thumb" :title="item.series" :type="item.type" />
                </div>
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

.series{
    width: 240px;
    padding: 8px;
    padding-top: 14px;
    background-color: $backgroundFooterTop;
    transform: translateY(-90%);
}

main {
    background-color: $backgroundMain;
    color: white;
    font-size: 3rem;
}

</style>