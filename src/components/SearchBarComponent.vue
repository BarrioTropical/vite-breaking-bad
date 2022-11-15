<template>
    
    <div class="container">
    <div>
    <select name="category" id="category" v-model="store.search.category">
    <option value="">Scegli la categoria</option>
    <option :value="category" v-for="(category, index) in categoryOptions" :key="index">{{ category }}</option>
  </select>
    </div>
    </div>
</template>

<script>
import { store } from '../store';
    export default {
        name: 'SearchBarComponent',

        data() {
        return {
            store,
            categoryOptions: [
                'Breaking Bad',
                'Better Call Saul',
                'unknown'
            ],


        }
    },
    methods: {
        searchCharacters() {
            this.$emit('filterchar');

            axios.get('https://www.breakingbadapi.com/api/characters',store.options).then((res)=>{
                console.log(res.data);
                setTimeout(()=>{
                    store.loading = false;
                    store.characters = [...res.data];
                },2000);
            })

        },
        resetSearch() {
            store.search.category = '';
            this.$emit('filterchar')

            
        }
    }

        }
</script>

<style lang="scss" scoped>

@use '../assets/styles/_partials/variables.scss' as *;
@use '../assets/styles/general.scss' as *;
    
    .container{
        padding-top: 30px;
        background-color: $grey;
    }


</style>