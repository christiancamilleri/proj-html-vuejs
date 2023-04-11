<script>
import CardItem from './CardItem.vue';

import { store } from '../store.js';


export default {
    data() {
        return {
            store,
            cards: [
                {
                    img: "course-02-480x298.jpg",
                    price: "$40.00",
                    description: "Learning to Write as a Professional Author",
                    details: "20 lessons 50 students"
                },
                {
                    img: "stock-full-hd-04-480x298.jpg",
                    price: "$19.00",
                    description: "Open Programming Courses for Everyone: Python",
                    details: "17 lessons 62 students"
                },
                {
                    img: "course-featured-image-01-480x298.jpg",
                    price: "$40.00",
                    description: "Master jQuery in a Short Period of Time",
                    details: "6 lessons 51 students"
                },
                {
                    img: "stock-full-hd-03-480x298.jpg",
                    price: "FREE",
                    description: "Customer Centric Info-Tech Strategies",
                    details: "24 lessons 769 students"
                },
                {
                    img: "stock-full-hd-06-480x298.jpg",
                    price: "$26.00",
                    description: "Academic Listening and Note-taking",
                    details: "14 lessons 67 students"
                },
                {
                    img: "stock-full-hd-05-480x298.jpg",
                    price: "$59.00",
                    description: "Introduction to Javascript for Beginners",
                    details: "14 lessons 76 students"
                },

            ]
        }
    },
    components: {
        CardItem,
    }
}
</script>

<template>
    <main>

        <div class="container">
            <div id="title">
                <small>
                    STIMULATED TO LEARN?
                </small>
                <h2>
                    Feautured Online Courses
                </h2>
            </div>
            <div id="card-container">

                <CardItem v-for="card in cards" :card="card"></CardItem>

            </div>
            <div id="btn">
                <button><b>View All Courses</b> <i class="fa-solid fa-arrow-right"></i> </button>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    background-color: #f5f7fa;
    margin-top: 5em;

    #title {
        text-align: center;
        padding-top: 5em;

        small {
            opacity: .4;
        }

        h2 {
            margin-top: 0;
        }
    }

    #card-container {
        display: flex;
        flex-flow: column wrap;
        align-items: center;

        gap: 2em;

        max-height: 500px;
    }

    #btn {
        text-align: center;
        margin-top: 2em;

        button {
            padding: 20px 40px;

            max-width: 60%;

            margin: 1em 0;

            border: none;

            color: white;

            border-radius: 8px;
            background-color: #20AD96;

            cursor: pointer;

        }

        button:hover {
            background-color: #3F3A64;
        }
    }


}
</style>