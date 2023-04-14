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
    <div id="back">

        <div class="container">
            <div id="img-container">
                <img id="main-img" src="/images/home-2-popup-video-poster.jpg" alt="">
                <img id="yt-btn" src="/images/icon-youtube-play.png" alt="">
                <img id="path1" src="/images/maxcoach-shape-07-150x150.png" alt="">
                <img id="path2" src="/images/maxcoach-shape-05.png" alt="">
                <img id="path3" src="/images/path3.png" alt="">
            </div>

            <div id="text-container">
                <i id="circle" class="fa-regular fa-circle"></i>
                <small>
                    <span>GET STARTED</span> <b>EFFORTLESSY</b>
                </small>

                <h2>
                    Enjoy Our
                    <br>
                    <span>Companionship</span>
                </h2>
                <p>
                    <small>
                        Sneek peek into what has in store for you on our online teaching and mentoring portal.Seek for some
                        hidden
                        hints of early-bird rewards as well.
                    </small>
                </p>

                <a href="#">Download free guidebook <i class="fa-solid fa-arrow-right"></i></a>

            </div>

        </div>

    </div>
</template>

<style lang="scss" scoped>
#back {

    background-color: white;

    border-radius: 0 0 400px 0;


    .container {
        display: flex;
        justify-content: space-between;
        gap: 1em;

        margin-top: 200px;
        padding-bottom: 5em;



        border-radius: 0 0 0 30px;

        #img-container {
            width: 60%;

            position: relative;

            #main-img {
                width: 100%;
                position: absolute;
                top: -10%;

                z-index: 5;

            }

            #yt-btn {
                position: absolute;
                top: 35%;
                right: 40%;

                z-index: 6;
            }

            #path1 {
                position: absolute;
                bottom: -20%;
                left: 76%;

            }

            #path2 {
                position: absolute;
                top: 12%;
                left: -14%;

                z-index: 1;

            }

            #path3 {
                position: absolute;
                top: -20%;
                left: -11%;

                width: 250px;
                height: 300px;
            }

        }

        #text-container {
            width: 40%;
            padding: 2em 1em;

            position: relative;

            #circle {
                position: absolute;
                top: -7%;
                left: -2%;
                font-size: 3em;

                color: #ecc5ab;
            }

            small {
                span {
                    opacity: .4;
                }
            }

            h2 {
                font-size: 2em;

                span {

                    color: #20AD96;
                }
            }

            p {
                opacity: .4;
            }

            a {
                color: #20AD96;
                text-decoration: underline;

                font-size: .8em;
            }
        }
    }
}
</style>