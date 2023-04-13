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
        <!-- testo -->
        <div id="text-container">
            <h1>
                Distant learning for further expansion
            </h1>
            <small>
                Learning is a life-long journey that in fact we never find the terminate stop. Stop searching enjoy the
                process.
            </small>
            <button>
                <i class="fa-solid fa-download"></i> <b>Download Free Guide</b>
            </button>
            <small>
                Have a question?
                <a href="#"> Get Free Sample <i class="fa-solid fa-arrow-right"></i> </a>
            </small>

        </div>

        <!-- immagine -->
        <div id="img-container">
            <img id="img0" src="/images/about-me-profile.jpg" alt="">
            <img id="img1" src="/images/maxcoach-shape-02.png" alt="">
            <img id="img2" src="/images/maxcoach-shape-07.png" alt="">
            <img id="img3" src="/images/maxcoach-shape-08.png" alt="">
            <img id="img4" src="/images/maxcoach-shape-08.png" alt="">
            <i id="circle" class="fa-regular fa-circle"></i>

        </div>
    </div>

    <!-- loghi -->
    <div id="logos">
        <img id="logo1" src="/images/client-logo-01.png" alt="">
        <img src="/images/client-logo-02.png" alt="">
        <img src="/images/client-logo-03.png" alt="">
        <img src="/images/client-logo-04.png" alt="">
        <img src="/images/client-logo-05.png" alt="">
        <img src="/images/client-logo-06.png" alt="">
    </div>
</template>

<style lang="scss" scoped>
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 2em;


    #text-container {
        width: 40%;

        display: flex;
        flex-direction: column;

        a {
            color: #20AD96;
        }

    }

    #img-container {
        width: 60%;
        padding: 50px 0;

        position: relative;

        #img0 {
            border-radius: 50%;
            height: 400px;
            margin-left: 120px;
        }

        #img1 {
            position: absolute;
            right: 2%;
            top: 25%;

            height: 60px;
        }

        #img2 {
            position: absolute;
            top: 75%;
            right: 22%;

            height: 60px;

            z-index: -1;
        }

        #img3 {
            position: absolute;
            left: 10%;
            top: 34%;

            z-index: -1;

            height: 80px;
        }

        #img4 {
            position: absolute;
            left: 10%;
            top: 53%;

            z-index: -1;

            height: 80px;
        }

        #circle {
            position: absolute;
            top: 63%;
            left: 18%;

            font-size: 2em;
            color: #ecc5ab;
        }
    }
}

#logos {
    max-width: 1000px;
    margin: 0 auto;

    display: flex;
    gap: 60px;

    img {
        height: 40px;
        opacity: .5;
    }

}
</style>