<script>
import { store } from '../store.js'

export default {
    data() {
        return {
            store,
        }
    }
}
</script>

<template>
    <div class="container">
        <img id="path1" src="/images/maxcoach-shape-02.png" alt="">
        <img id="path2" src="/images/maxcoach-shape-09.png" alt="">
        <i id="path3" class="fa-regular fa-circle"></i>
        <div class="title">
            <b>Subscribe</b> <span>Newsletters</span>
        </div>
        <div class="description">
            Enter your email address to register to our Newsletter subscription delivered on a regular basis!
        </div>
        <div class="input-container">

            <input type="email" placeholder="Enter Your Email" name="" id="">
            <button id="subscribe">
                Subscribe
            </button>

        </div>
    </div>
</template>

<style lang="scss" scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;

    padding: 5em;

    text-align: center;

    position: relative;

    #path1 {
        position: absolute;
        top: 52%;
        right: 12%;

        height: 80px;
    }

    #path2 {
        position: absolute;
        top: 23%;
        right: 12%;

        height: 140px;
    }

    #path3 {
        position: absolute;
        top: 50%;
        left: 10%;

        color: #8fd6c9;

        font-size: 2.5em;
    }

    .title {
        font-size: 2em;

        span {
            color: #20AD96;
        }
    }

    .description {
        padding: 1.5em 0;

        opacity: .5;

        max-width: 490px;

    }

    .input-container {
        display: flex;
        justify-content: center;
        width: 100%;



        input {
            background-color: #f5f5f5;
            border: none;
            width: 40%;

            padding: 0 10px;
        }

        #subscribe {
            height: 100%;

            margin: 0;

            border-radius: 5px;
        }
    }

}
</style>