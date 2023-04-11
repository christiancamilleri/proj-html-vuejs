<script>
import { store } from '../store.js'
export default {
    data() {
        return {
            store,
            links: [
                {
                    name: "Home",
                    drop_links: [
                        "Start here",
                        "Success Story",
                        "About me",
                        "About us 01",
                        "About us 02",

                    ]
                },
                {
                    name: "Pages",
                    drop_links: [
                        "Start here",
                        "Success Story",
                        "About me",
                        "About us 01",
                        "About us 02",
                        "About us 03",
                        "About us 04",
                    ]
                },
                {
                    name: "Courses",
                    drop_links: [
                        "Start here",
                        "Success Story",
                        "About me",
                        "About us 01",
                        "About us 02",

                    ]
                },
                {
                    name: "Feautures",
                    drop_links: [
                        "Start here",
                        "Success Story",
                        "About me",
                        "About us 01",
                        "About us 02",
                        "About us 03",
                        "About us 04",
                    ]
                },
                {
                    name: "Blog",
                    drop_links: [
                        "Start here",
                        "Success Story",
                        "About me",
                        "About us 01",

                    ]
                },
                {
                    name: "Shop",
                    drop_links: [

                        "About us 01",
                        "About us 02",
                        "About us 03",
                        "About us 04",
                    ]
                },

            ]
        }
    }
}
</script>

<template>
    <nav>
        <div class="container">

            <!-- logo -->
            <div id="logo">
                <img src="/images/dark-logo.png" alt="">
            </div>

            <!-- lista links -->
            <div id="links">

                <ul>
                    <li v-for="link in links" class="links"> <a href="#">{{ link.name }} </a>
                        <i class="fa-solid fa-angle-down"></i>

                        <!-- drop menu -->
                        <ul id="drop-down-menu">
                            <li v-for="link in link.drop_links"> <a href="#">{{ link }}</a> </li>
                        </ul>

                    </li>

                </ul>
            </div>

            <!-- user-icon -->
            <div class="icon">
                <i class="fa-regular fa-circle-user"></i>
            </div>

            <!-- search-bar  -->
            <div id="input">
                <input type="text" placeholder="search...">
                <i class="fa-sharp fa-solid fa-magnifying-glass"></i>
            </div>

        </div>

    </nav>
</template>

<style lang="scss" scoped>
nav {
    box-shadow: 0 10px 15px rgba(0, 0, 0, 0.044);


    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        gap: 20px;



        .fa-solid {
            font-size: .7em;
            color: #4c4c4c;
        }

        #logo {

            padding: 10px;

            img {
                max-width: 200px;
            }
        }

        ul {
            display: flex;
            gap: 20px;

            li {
                display: flex;
                align-items: center;
                gap: 5px;

                position: relative;

                #drop-down-menu {
                    position: absolute;
                    top: 120%;
                    left: 0;
                    display: none;

                    width: 120px;

                    border-bottom: 2px solid #20AD96;
                    z-index: 2;


                    li {
                        padding: 10px 30px 10px 10px;
                        margin-left: -40px;

                        color: #4c4c4c;

                    }
                }
            }
        }

        .links:hover {
            color: #20AD96;

            border-bottom: 2px solid #20AD96;
        }

        li:hover #drop-down-menu {
            display: flex;
            flex-direction: column;

            gap: 0;

            background-color: white;
        }

        #input {

            display: flex;
            position: relative;

            input {
                width: 90%;
                padding: 15px;

                border: none;

                background-color: #f5f5f5;


            }

            i {
                font-size: 1em;

                position: absolute;
                right: 20px;
                top: 15px;


                color: #20AD96;
            }

        }

    }
}
</style>