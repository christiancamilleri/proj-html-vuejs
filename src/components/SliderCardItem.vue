<script>
export default {
    data() {
        return {

        }
    },
    props: {
        card: Object,
    }
}
</script>

<template>
    <div class="card">
        <p id="title">
            <b>{{ card.title }}</b>
        </p>
        <p id="description">
            {{ card.description }}
        </p>
        <div id="card-bottom">
            <img :src="`/images/${card.img}`" alt="">

            <div>

                <span>
                    <b>{{ card.name }}</b>
                </span>

                <div id="work">
                    {{ card.work }}
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.card {
    width: calc(100% / 3 - 2em / 3 * 2);
    height: 300px;
    padding: 2em;

    background-color: white;

    #description {
        opacity: .7;
    }

    #card-bottom {
        display: flex;
        align-items: center;
        gap: .5em;

        img {
            height: 60px;
            width: 60px;

            border-radius: 50%;
        }

        div {

            #work {
                font-size: .5;

                opacity: .4;
            }
        }

    }

}
</style>