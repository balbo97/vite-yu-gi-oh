<script>
import { store } from '../store'
import axios from 'axios';

export default {
    name: 'AppSelect',

    data() {
        return {
            store,

            archetypeArray: [
                'Alien',
                'Infernoble Arms',
                'Noble Knight',
                'Melodious',
                'Archfiend'

            ]
        }
    },


}
</script>

<template lang="">
    <div class="container mb-5">

        <select class="form-select-sm" aria-label="Default select example" v-model="store.archetype">
           
            <option v-for="archetype, index in archetypeArray" :key="index" :value="archetype">
             {{archetype}}
            </option>
           
        </select>
        <div class="btn btn-success ms-1">Invio</div>
    </div>
</template>

<style lang="">
    
</style>