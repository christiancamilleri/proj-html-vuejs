<script>
import { store } from '../store.js'

export default {
    data() {
        return {
            store,

            lista1: [
                "382 NE 191st ST# 87394 Miami, FL 33179-3899",
                "+1(305) 547-9909 (9am-5pm EST, Monday-Friday)",
                "support@maxcoach.com"
            ],

            lista2: [
                "Start here",
                "Blogs",
                "About us",
                "Success Story",
                "Courses",
                "Contact us"
            ],

            lista3: [
                "Membership",
                "Purchase guide",
                "Privacy polices",
                "Therms of services"

            ]


        }
    }
}
</script>

<template>
    <footer>

        <div class="container">
            <div class="footer-left">
                <div class="lista">
                    <h3>
                        Address
                    </h3>
                    <ul class="list-1">
                        <li v-for="item in lista1">{{ item }}</li>

                    </ul>
                </div>

                <div id="social">
                    <i class="fa-brands fa-facebook icon"></i>
                    <i class="fa-brands fa-twitter icon"></i>
                    <i class="fa-brands fa-instagram icon"></i>
                    <i class="fa-brands fa-linkedin icon"></i>

                </div>
            </div>
            <div class="footer-right">

                <div class="lista">
                    <h3>
                        Explore
                    </h3>
                    <ul class="list-2">
                        <li v-for="item in lista2"> {{ item }}</li>

                    </ul>
                </div>

                <div class="lista">
                    <h3>
                        Information
                    </h3>
                    <ul class="list-1">
                        <li v-for="item in lista3">{{ item }}</li>
                    </ul>
                </div>
            </div>
        </div>

        <button id="go-up">
            <a href="#"><i class="fa-solid fa-arrow-up"></i></a>
        </button>

        <div class="footer-bottom">
            <span>© 2020 Maxcoach. All Right Reserved</span>
        </div>

    </footer>
</template>

<style lang="scss" scoped>
footer {
    background-color: #f8f8f8;
    position: relative;

    .container {
        display: flex;
        justify-content: space-between;

        padding: 2em;

        .footer-left {
            #social {
                display: flex;
                gap: 1em;

                color: #b1b1b1;
            }
        }

        .list-1 {
            padding: 0;
        }

        li {
            padding: 5px;
            color: #b1b1b1;
        }

        li:hover {
            color: #20AD96;

            cursor: pointer;
        }

        .footer-right {
            display: flex;
            gap: 7em;

            margin-right: 5em;

            .lista {
                display: flex;
                flex-direction: column;
                align-items: flex-start;

                h3 {
                    margin: 0;
                }

                .list-2 {
                    display: flex;
                    flex-flow: column wrap;
                    height: 102px;

                    padding: 0;
                    gap: 0 10px;
                }
            }
        }
    }

    #go-up {
        border-radius: 50%;
        position: absolute;
        bottom: 0;
        right: 0;
    }

    .footer-bottom {
        display: flex;
        justify-content: center;

        opacity: .4;

        padding-bottom: 2em;

        font-size: .8em;
    }
}
</style>