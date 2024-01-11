<script>
import { store } from './store'
import axios from 'axios';

import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
export default {
  components: {

    AppHeader,
    AppMain

  },
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

<template lang="">
  <div>
    <AppHeader />
    <AppMain />
  </div>
</template>

<style lang="scss">
@use './styles/general' as *;
</style>
