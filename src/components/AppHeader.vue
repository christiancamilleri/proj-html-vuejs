<script>
import NavBar from './NavBar.vue';

import { store } from '../store.js'


export default {
    data() {
        return {
            store,
        }
    },
    components: {
        NavBar,
    }
}
</script>

<template>
    <div>
        <NavBar></NavBar>
    </div>
</template>

<style lang="scss" scoped></style>