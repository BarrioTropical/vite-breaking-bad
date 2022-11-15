<template>
    <div>
        <div v-html="`found ${characterList.length} characters`"></div>
        <ProductComponent :character="characterList" />
    </div>
</template>

<script>
import axios from 'axios'
import ProductComponent from './ProductComponent.vue';


export default {
    components: {
ProductComponent,}, 
    data() {
        return {
            apiURL: 'https://www.breakingbadapi.com/api/characters',
            characterList: [],
            loading: false
        }
    },
    methods: {

        getCharacters() {
            // this.loading = true;
            axios.get(this.apiURL).then(
                (res) => {
                    this.characterList = [...res.data]
                },

            )
                .catch((error) => {

                    console.log(error);
                })
        }
    },
    created() {
        this.getCharacters()
    }
}

</script>

<style lang="scss" scoped>

</style>