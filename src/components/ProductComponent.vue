<template>
    <div class="container">
        <div class="d-flex">
            <div class="column product" v-for="(item, index) in character " :key="item.char_id">
                <img :src="item.img" :alt="item.name">
                <h2 class="mt-2 text-white">{{ item.name }}</h2>
                <h5 class="text-secondary">{{ item.category }}</h5>
                <p class="text-secondary">{{ item.status }}</p>
            </div>
        </div>

    </div>
</template>

<script>
    export default {
        name: 'ProductComponent',
        props: [
        'character'
        ],
    }
</script>

<style lang="scss" scoped>
    @use '../assets/styles/_partials/variables.scss' as *;
    @use '../assets/styles/general.scss' as *;

    .product {
    margin: 0 10px;
    background-color: $grey;
    max-width: 400px;
    padding: 10px;
    
        h2{
            text-transform: uppercase;
            color: $white;
        }

}

.d-flex{
    display: flex;
    flex-direction: column;
    align-items: inherit;
    justify-content: flex-start;
    flex-flow: row wrap;
}

.column{
    width: 17%;
    margin: 0 auto;
    margin-bottom: 20px;
}

    h2,
    h5,
    p{
        color: $greydark;
        font-size: 15px;
        text-align: center;
    }
</style>