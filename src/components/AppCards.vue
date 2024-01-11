<script>


import { store } from '../store'
export default {
    name: 'AppCards',
    data() {
        return {
            store
        }
    },

}
</script>
r
<template lang="">
    <div class="container">
        <div class="row">
            
            <div class="col-12 col-md-6 col-lg-3" v-for="(card, index) in store.cardsList" :key="index">
                <div class="cards">
                    <img :src="card.card_images[0].image_url" alt="">
                    <h5>{{card.name}}</h5>
                    <p>{{card.archetype}}</p>
                </div>
            </div>
        </div>

    </div>
</template>

<style lang="scss" scoped>
.container {
    background-color: white;


    .card-count {
        background-color: black;
    }

    .cards {

        background-color: orange;
        text-align: center;





        img {
            max-width: 100%;
        }

        h5 {
            text-transform: uppercase;
            color: white;
            padding-top: 20px;
            font-weight: bold;
        }

    }

}
</style>