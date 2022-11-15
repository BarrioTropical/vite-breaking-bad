<template>
    
    <div class="container">
    <div>
    <select name="category" id="category">
    <option value="null">Better Call Saul</option>
    <option value="null">Breaking Bad</option>
  </select>
    </div>
    </div>
</template>

<script>
    export default {
        name: 'SearchBarComponent'
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