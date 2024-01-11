<script>
export default {
    name: 'AppHeader'

}
</script>

<template lang="">
   <header>
    <div class="container-fluid d-flex">

        <img src="https://upload.wikimedia.org/wikipedia/commons/1/11/Yu-Gi-Oh%21_%28Logo%29.jpg" alt="">
        <h1>Yu-Gi-Oh Api</h1>
    </div>
   
   </header>
</template>

<style lang="scss">
header {
    height: 75px;
    display: flex;

    h1 {
        display: flex;
        align-items: center;
    }


    img {
        max-width: 100%;
        max-height: 100%;
    }

}
</style>