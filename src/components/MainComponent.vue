<template>
    <div class="container">
        <div class="whitebox">
            <div class="result-box">Found XX chaacters</div>
        
        </div>
    </div>
</template>

<script>
    export default {
        name: 'MainComponent'
    }
</script>

<style lang="scss" scoped>
    @use '../assets/styles/_partials/variables.scss' as *;
    @use '../assets/styles/general.scss' as *;

    .whitebox{
        background-color: $white;
        padding: 30px;
    }

    .result-box{
        background-color: $greydark;
        color: $white;
        padding: 10px;
    }

</style>