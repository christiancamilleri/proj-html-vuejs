<script>
import { store } from '../store.js'

export default {
    data() {
        return {
            store,
        }
    },
    props: {
        card: Object
    }
}
</script>

<template>
    <div id="container">
        <img :src="`/images/${card.img}`" alt="">
        <div id="text-container">
            <div class="price">
                <b>{{ card.price }}</b>
            </div>
            <div class="description">
                {{ card.description }}
            </div>
            <div class="details">
                <span>
                    <i class="fa-regular fa-file"></i> {{ card.details1 }}
                </span>
                <span>
                    <i class="fa-regular fa-user"></i> {{ card.details2 }}
                </span>
            </div>
        </div>

    </div>
</template>

<style lang="scss" scoped>
#container {
    display: flex;
    gap: 1rem;

    max-width: 400px;

    img {
        height: 120px;
        width: 120px;

        border-radius: 50%;

        object-fit: cover;

    }

    #text-container {

        padding-top: 10px;

        .price {
            color: #20AD96;
            font-size: 1.2em;
        }

        .description {
            padding: .8em 0;
        }

        .details {
            opacity: .5;
            font-size: .6em;

            display: flex;
            gap: 10px;
        }
    }
}
</style>