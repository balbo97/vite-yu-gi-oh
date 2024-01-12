<script>

import AppCards from './AppCards.vue'
import AppSelect from './AppSelect.vue';

export default {
    name: 'AppMain',
    components: {
        AppCards,
        AppSelect

    }


}
</script>

<template lang="">
    <main>
        <!-- SELECT BAR  -->
        <AppSelect />
        <!-- CARDS -->
         <AppCards />
    </main>
</template>

<style lang="scss" scoped></style>