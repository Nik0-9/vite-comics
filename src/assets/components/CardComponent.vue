<template>
    <div>
        <img :src="image" :alt="type" class=" image-fluid w-100 ">
        <div class="">
            <h5 class="text-uppercase pt-2">{{title}}</h5>
            <h6>{{price}}</h6>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'CardComponent',
        props: ['image', 'type', 'title','price']
    }
</script>

<style lang="scss" scoped>
img{
    max-height: 250px;
}
</style>