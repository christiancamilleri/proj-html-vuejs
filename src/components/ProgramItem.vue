<script>
import { store } from '../store.js';

export default {
    data() {
        return {
            store,
        }
    },
    props: {
        item: Object,
    }
}
</script>

<template>
    <div id="container">
        <img :src="`/images/${item.img}`" alt="">
        <h3>
            {{ item.title }}
        </h3>
        <small>
            {{ item.description }}
        </small>
        <div>
            <a href="#"><b>{{ item.action }}</b> <i class="fa-solid fa-arrow-right"></i></a>
        </div>

    </div>
</template>

<style lang="scss" scoped>
#container {
    max-width: 250px;


    div {
        margin-top: 1em;

        font-size: .8em;

        opacity: .4;
    }
}
</style>