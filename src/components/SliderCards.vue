<script>
import { store } from '../store.js';

import SliderCardItem from './SliderCardItem.vue';

export default {
    data() {
        return {
            store,
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
                {
                    title: "It's a choice of quality for people with special needs",
                    description: "I m a very strict person so i require everything to be organized and neat.Then, i'll be able to make things right and shine.MaxCoach guys just got me",
                    img: "testimonial-avata-01.jpg",
                    name: "FLORENCE THEMES",
                    work: "/ MULTIMEDIA ADMIN"
                },

            ],
            activeIndex: 0,
            activeLess: 3,
            activePlus: 1,
        }
    },
    methods: {
        ChangeSlide(index) {
            this.activeIndex = index

            this.slideDisplay()
        },
        slideDisplay() {
            if (this.activeIndex == 0) {
                this.activeLess = this.cards.length - 1;
                this.activePlus = this.activeIndex + 1;
            } else if (this.activeIndex == this.cards.length - 1) {
                this.activeLess = this.activeIndex - 1;
                this.activePlus = 0
            } else {
                this.activeLess = this.activeIndex - 1;
                this.activePlus = this.activeIndex + 1
            }
        }
    },
    components: {
        SliderCardItem,
    },
    mounted() {
        this.slideDisplay()
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
    <div class="card-container">

        <SliderCardItem @click="ChangeSlide(activeLess)" :card="cards[activeLess]" class="inactive"></SliderCardItem>
        <SliderCardItem :card="cards[activeIndex]" class="active"></SliderCardItem>
        <SliderCardItem @click="ChangeSlide(activePlus)" :card="cards[activePlus]" class="inactive"></SliderCardItem>

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

.card-container {
    display: flex;
    gap: 2em;

    margin-top: 3em;

    background-color: #f7f7f7;

    height: 100%;
    width: 100%;
}

#slider {
    display: flex;
    gap: .5em;
    justify-content: center;

    margin-top: 3em;

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

    padding-bottom: 3em;

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