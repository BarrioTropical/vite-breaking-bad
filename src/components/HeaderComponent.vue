<template>
    <header>
    <div class="logo p-3">
    Breaking Bad Api
    </div>

    <div class="container pt-3">
        <select name="category" id="category">
    <option value="null">Select category</option>
    <option value="null">Select category</option>
    <option value="null">Select category</option>
    <option value="null">Select category</option>
  </select>
    </div>
    </header>
</template>

<script>
    export default {
        name: 'HeaderComponent'
    }
</script>

<style lang="scss" scoped>
    @use '../assets/styles/_partials/variables.scss' as *;
    @use '../assets/styles/general.scss' as *;

    .logo{
        color: $white;
        padding: 40px;
        font-size: 30px;
    }

    header{
    background-color: #2E3A46;
    padding: 40px;
  }

</style>