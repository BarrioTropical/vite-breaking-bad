<template>
    
    <header>
        <div>
            <a href="#">
                <img src="../../public/logo.png" width="50" alt="Breaking Bad"> Breaking Bad Api
            </a>
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

        a{
            color: white;
            font-size: 30px;
            text-decoration: none;
        }

  }

</style>