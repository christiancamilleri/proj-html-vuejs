<script>
import { store } from '../store.js'

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
    <div class="item">
        <b>{{ item.title }}</b>

        <span>
            <b>{{ item.number }}</b>
        </span>
        <small>
            {{ item.student }}
        </small>
    </div>
</template>

<style lang="scss" scoped>
.item {
    width: calc(100% / 4);


    border-left: 1px solid #f1ebe5;

    padding: 60px;

    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1em;

    text-align: center;

    span {
        font-size: 3em;
        color: #20AD96;
    }

    small {
        opacity: .4;
    }

}
</style>