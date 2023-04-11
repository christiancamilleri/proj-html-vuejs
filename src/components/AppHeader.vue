<script>
import NavBar from './NavBar.vue';
import jumbo from './jumbo.vue';

import { store } from '../store.js'


export default {
    data() {
        return {
            store,
        }
    },
    components: {
        NavBar,
        jumbo,
    }
}
</script>

<template>
    <div>
        <NavBar></NavBar>
        <jumbo></jumbo>
    </div>
</template>

<style lang="scss" scoped></style>