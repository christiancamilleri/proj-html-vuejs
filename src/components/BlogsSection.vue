<script>
import { store } from '../store.js';

export default {
    data() {
        return {
            store,

            blogsCards: [
                {
                    img: "/images/artist-blog-03-480x352.jpeg",
                    work: "Artist",
                    description: "Brush Strokes Energize Trees in Paintings",
                    info1: "May, 15 2020",
                    info2: "688 views"
                },
                {
                    img: "/images/artist-blog-01-480x352.jpg",
                    work: "Artist",
                    description: "Pocket-Sized Notebooks Hold Miniature Paintings",
                    info1: "May, 15 2020",
                    info2: "603 views"
                },
            ]
        }
    },

}
</script>

<template>
    <div id="background">

        <div class="container">
            <div class="text">
                <small class="mini-title">
                    ENJOYABLE INSIGHT
                </small>
                <div class="title">
                    <h3>
                        Most Viewed <span>Best Blogs</span>
                    </h3>
                </div>
                <ul>
                    <li><i class="fa-solid fa-arrow-right"></i><small>Become a Better Blogger: Content Planning</small>
                    </li>
                    <li><i class="fa-solid fa-arrow-right"></i><small>Promoting your Online Business On Pinterest</small>
                    </li>
                    <li><i class="fa-solid fa-arrow-right"></i><small>Gamification and Game-Based Learning</small> </li>
                    <li><i class="fa-solid fa-arrow-right"></i><small>Designing an Online Course from Expert's
                            Perspective</small> </li>
                    <li><i class="fa-solid fa-arrow-right"></i><small>Why Online Courses are the Future od Education</small>
                    </li>
                </ul>
            </div>

            <div v-for="card in blogsCards" class="card">
                <img :src="`${card.img}`" alt="">
                <div class="card-info">
                    <small class="work">
                        {{ card.work }}
                    </small>
                    <span>
                        {{ card.description }}
                    </span>
                    <small class="info">
                        <span><i class="fa-regular fa-calendar"></i> {{ card.info1 }}</span>
                        <span><i class="fa-solid fa-eye"></i> {{ card.info2 }}</span>
                    </small>

                </div>
            </div>

        </div>

    </div>
</template>

<style lang="scss" scoped>
#background {
    background-color: #f5f1ed;

    .container {
        display: flex;
        gap: 2em;

        padding-top: 3em;

        .text {
            width: 40%;

            padding: 2em;

            .mini-title {
                opacity: .4;
            }

            .title {
                span {
                    color: #20AD96;
                }
            }

            ul {
                padding-left: 0;


                li {
                    display: flex;
                    align-items: center;
                    gap: 20px;

                    padding: 10px;

                    i {
                        font-size: .8em;
                    }

                    small {
                        font-size: .6em;
                        font-weight: bold;
                    }
                }
            }
        }

        .card {
            width: 30%;

            display: flex;
            flex-direction: column;

            background-color: white;

            margin-bottom: 2em;

            .card-info {
                display: flex;
                flex-direction: column;

                padding: 1em;

                small {
                    opacity: .4;
                }

                .work {
                    font-weight: bold;
                }

                span {
                    padding: 1em 0;
                }

                .info {
                    font-size: .7em;

                    display: flex;
                    gap: 20px;
                }



            }
        }

    }
}
</style>