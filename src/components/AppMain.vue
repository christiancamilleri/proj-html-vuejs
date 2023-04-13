<script>
import CardItem from './CardItem.vue';
import ProgramItem from './ProgramItem.vue';
import CompanionItem from './CompanionItem.vue';
import SliderCards from './SliderCards.vue';
import StatisticsItem from './StatisticsItem.vue';

import { store } from '../store.js';


export default {
    data() {
        return {
            store,
            cards: [
                {
                    img: "course-02-480x298.jpg",
                    price: "$40.oo",
                    description: "Learning to Write as a Professional Author",
                    details: "20 lessons 50 students"
                },
                {
                    img: "stock-full-hd-04-480x298.jpg",
                    price: "$19.oo",
                    description: "Open Programming Courses for Everyone: Python",
                    details: "17 lessons 62 students"
                },
                {
                    img: "course-featured-image-01-480x298.jpg",
                    price: "$40.oo",
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
                    price: "$26.oo",
                    description: "Academic Listening and Note-taking",
                    details: "14 lessons 67 students"
                },
                {
                    img: "stock-full-hd-05-480x298.jpg",
                    price: "$59.oo",
                    description: "Introduction to Javascript for Beginners",
                    details: "14 lessons 76 students"
                },

            ],
            ProgramItems: [
                {
                    img: "home-2-image-box-01.png",
                    title: "Customize Preferences",
                    description: "Learners are given the right to arrange and customize their study schedule and timetable based on preferences",
                    action: "Start here"
                },
                {
                    img: "about-us-02-image-box-02.png",
                    title: "Cloud Storage",
                    description: "You can store online lessons via online cloud or download to your device and revise lessons on the way.",
                    action: "Get free quote"
                },
                {
                    img: "home-2-image-box-03.png",
                    title: "Multimedia Channels",
                    description: "We provide study materials with varios formats:video, audio, slides, doc, prints,books and applications.",
                    action: "Start now"
                },
            ],
            statisticItems: [
                {
                    title: "Successfully trained",
                    number: "1790",
                    student: "ENROLLED LEARNERS"
                },
                {
                    title: "Proudly Received",
                    number: "19",
                    student: "COUNTRYWIDE AWARDS"
                },
                {
                    title: "Firmly Established",
                    number: "24",
                    student: "LOCAL BRANCHES"
                },
                {
                    title: "Getting Feautured On",
                    number: "1090",
                    student: "BLOG POSTS"
                },
            ]
        }
    },
    components: {
        CardItem,
        ProgramItem,
        CompanionItem,
        SliderCards,
        StatisticsItem,
    }
}
</script>

<template>
    <main>
        <section>
            <!-- card section -->
            <div class="container">
                <div class="title">
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
                <!-- /card section -->
            </div>
        </section>
        <div class="container">
            <!-- program section -->
            <div class="title">
                <small>
                    MAXCOACH AVAILABLE COURSES
                </small>
                <h2>
                    Access <span>Smart Tutoring</span> Program For Benefits.
                </h2>
            </div>
            <div id="program-item-container">
                <ProgramItem v-for="programItem in ProgramItems" :item="programItem"></ProgramItem>
            </div>
            <!-- /program section -->

        </div>

        <div id="background">
            <!-- companion section -->
            <CompanionItem></CompanionItem>
            <!-- /companion section -->

            <!-- slider cards section -->
            <SliderCards></SliderCards>
            <!-- /slider cards section -->
        </div>
        <!-- statistic section -->
        <div class="container statistic">

            <StatisticsItem v-for="item in statisticItems" :item="item"></StatisticsItem>

        </div>
        <!-- /statistic section -->

    </main>
</template>

<style lang="scss" scoped>
main {
    section {
        background-color: #f5f7fa;
        margin-top: 5em;
        padding-bottom: 5em;



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

        }

    }

    .title {
        text-align: center;
        padding-top: 5em;

        small {
            opacity: .4;
        }

        h2 {
            margin-top: 0;

            span {
                color: #20AD96;

            }
        }
    }



    #program-item-container {
        display: flex;
        justify-content: space-between;
        margin-top: 4em;
    }

    #background {
        background-color: #f7f7f7;
    }

    .statistic {
        display: flex;
    }

    .statistic:last-child {
        border-right: 1px solid #f1ebe5;
        ;
    }

}
</style>