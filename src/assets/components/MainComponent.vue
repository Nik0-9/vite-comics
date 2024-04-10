<template>
    <main class="container">
    -- >Content goes here< --
    </main>
</template>

<script>
    export default {
        name: 'MainComponent'
    }
</script>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

main{
    background-color: $backgroundMain;
    color: white;
    font-size: 3rem;
    height: 150px;
}
</style>