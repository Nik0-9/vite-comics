<template>
    <div class="m-3 text-center">
    <img :src="image" :alt="type" class="p-3">
    <h5 class="text-uppercase pt-2">{{title}}</h5>
    </div>
</template>

<script>
    export default {
        name: 'CardComponent',
        props: ['image', 'type', 'title']
    }
</script>

<style lang="scss" scoped>
img{
    width: 200px;
    height: 250px;
}
</style>