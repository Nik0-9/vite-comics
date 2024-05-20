<template>
    <div>
        <img :src="image" :alt="type" class=" image-fluid w-100 ">
        <div class="">
            <h5 class="text-uppercase pt-2">{{title}}</h5>
            <div>
                <h6>{{price}}</h6>
                <button @click="remove(index)">Remove</button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'CardComponent',
        props: ['image', 'type', 'title','price'],
    
    methods:{
        remove(index){
            this.$emit('remove', index)
        }
    }
}
</script>

<style lang="scss" scoped>
img{
    max-height: 250px;
    transition: 0.5s;
&:hover{
    opacity: 0.6;
    }
}

</style>