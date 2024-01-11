<script>

import axios from 'axios';
import { store } from '../store'
export default {
    name: 'AppCards',
    data() {
        return {
            store
        }
    },
    methods: {
        getCards() {
            axios.get(store.endpoint).then((response) => {

                this.store.cardsList = response.data.data
            })
        }
    },
    created() {
        this.getCards();
    },
}
</script>
r
<template lang="">
    <div class="container">
        <div class="row">
            <div class="card-count">{{store.lenght}}</div>
            <div class="col-12 col-md-6 col-lg-3" v-for="(card, index) in store.cardsList" :key="index">
                <div class="cards" v-for="(image, index) in card.card_images" :key="index">
                    <img :src="image.image_url" alt="">
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