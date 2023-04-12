<script>
import { store } from '../store.js';

export default {
    data() {
        return {
            store,
            activeIndex: 1,
            cards: [
                {
                    title: "High level of efficiency and scientific teaching methods",
                    description: "I am free to learn at my own space, follow my own schedule and choose the subject i want to learn from the syllabus. Great study portal for people like me.",
                    img: "testimonial-avata-02.jpg",
                    name: "MINA HOLLACE",
                    work: "/ Freelancer"
                },
                {
                    title: "Professional team of specialist and passionate mentors at reach",
                    description: "I need to get a certification for english proficiency and MaxCoach is my best choise. Their tutor are smart and professional when dealing with students",
                    img: "testimonial-avata-04.jpg",
                    name: "MADLEY PONDOR",
                    work: "/ IT Specialist"
                },
                {
                    title: "It's a choice of quality for people with special needs",
                    description: "I m a very strict person so i require everything to be organized and neat.Then, i'll be able to make things right and shine.MaxCoach guys just got me",
                    img: "testimonial-avata-03.jpg",
                    name: "FLORENCE THEMES",
                    work: "/ MULTIMEDIA ADMIN"
                },

            ]
        }
    },
    methods: {
        ChangeSlide(index) {
            this.activeIndex = index
        }
    }
}
</script>

<template>
    <!-- titolo iniziale -->
    <div id="title-section">
        <small>
            GREAT WORDS ABOUT MAXCOACH
        </small>
        <h2>
            Our <span>top learners'</span> verbatim
        </h2>
    </div>
    <!-- /titolo iniziale -->

    <!-- cards -->
    <div id="card-container">
        <transition-group>

            <div id="card" v-for="(card, index) in cards" :key="index"
                :class="this.activeIndex == index ? `active` : `inactive`" @click="ChangeSlide(index)">
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
        </transition-group>
    </div>
    <!-- /cards -->

    <!-- point slide -->
    <span id="slider">
        <i v-for="(card, index) in cards" :key="index" class="fa-solid fa-circle" @click="ChangeSlide(index)"
            :class="this.activeIndex == index ? `active` : `inactive`"></i>
    </span>
    <!-- /point slide -->

    <!-- slider footer -->
    <div id="slider-footer">
        <p>
            <b>Start today for getting</b> <span>Online Certification</span>
        </p>
        <h3>
            You can be vour own guiding star with our help!
        </h3>

        <button>
            <b>Get started now</b>
        </button>

        <img id="path1" src="/images/maxcoach-shape-02.png" alt="">
        <img id="path2" src="/images/maxcoach-shape-01.png" alt="">
        <i id="path3" class="fa-regular fa-circle"></i>
    </div>
</template>

<style lang="scss">
#title-section {
    text-align: center;

    margin-top: 3em;

    small {
        opacity: .4;
    }

    h2 {
        span {
            color: #20AD96
        }
    }
}

#card-container {
    display: flex;
    justify-content: space-between;

    margin-top: 3em;

    gap: 2em;

    padding: 2em;

    background-color: #f7f7f7;



    #card {
        width: calc(100% / 3 - 2em / 3 - 2);

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

}

#slider {
    display: flex;
    gap: .5em;
    justify-content: center;

    margin-top: 2em;

    i:hover {
        cursor: pointer;
        color: gray;
    }

}

.active {

    opacity: 1;

    transform: scale(1.2)
}

.inactive {
    opacity: 0.2;

}

#slider-footer {
    display: flex;
    flex-direction: column;
    align-items: center;

    margin-top: 4em;

    position: relative;

    p {
        margin-bottom: 0;

        span {
            color: #20AD96;
        }
    }

    h3 {
        margin-top: 0;
    }

    button {
        padding: 10px 20px;

        max-width: 60%;

        margin: 1em 0;

        border: none;

        color: white;
        background-color: #20AD96;
    }

    button:hover {
        background-color: #3F3A64;
        cursor: pointer;
    }

    #path1 {
        position: absolute;
        top: 10%;
        right: 23%;
    }

    #path2 {
        position: absolute;
        top: 46%;
        left: 25%;

    }

    #path3 {
        position: absolute;
        top: 26%;
        left: 26%;

        font-size: 2em;

        color: #e6dcd2;
    }
}
</style>