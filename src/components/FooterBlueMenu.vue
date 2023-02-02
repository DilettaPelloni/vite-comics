<script>
    export default {
        name: 'FooterBlueMenu',
        data() {
            return {
                blueMenuContent: [
                    {
                        img: 'buy-comics-digital-comics.png',
                        title: 'digital comics',
                        link: '#',
                    },
                    {
                        img: 'buy-comics-merchandise.png',
                        title: 'dc merchandise',
                        link: '#',
                    },
                    {
                        img: 'buy-comics-subscriptions.png',
                        title: 'subscription',
                        link: '#',
                    },
                    {
                        img: 'buy-comics-shop-locator.png',
                        title: 'comic shop locator',
                        link: '#',
                    },
                    {
                        img: 'buy-dc-power-visa.svg',
                        title: 'dc power visa',
                        link: '#',
                    },
                ],//blueMenuContent
            };//return
        },//data
        methods: {
            getImgPath(img) {
                return new URL(`../assets/img/${img}`, import.meta.url).href;
            },//getImgPath
        },//methods
    }
</script>

<template>

    <div class="blue-menu">
        <div class="container">
            <ul>
                <li v-for="item in blueMenuContent">
                    <a :href="item.link">
                        <img :src="getImgPath(item.img)" :alt="item.title">
                        <span>{{item.title}}</span>
                    </a>
                </li>
            </ul>
        </div><!-- CHIUSURA CONTAINER -->
    </div><!-- CHIUSURA BLUE-MENU -->

</template>

<style lang="scss" scoped>
    @import "../style/partials/colors.scss";

    .blue-menu {
        padding: 3rem;
        background-color: $dc-blue;
        ul {
            list-style: none;
            display: flex;
            justify-content: space-around;
            li {
                color: white;
                a {
                    display: flex;
                    align-items: center;
                    text-transform: uppercase;
                    &:hover {
                        text-decoration: underline;
                    }
                    img {
                        margin-right: 1rem;
                        height: 60px;
                        max-width: 65px;
                    }//img
                }//a
            }//li
        }//ul
    }//blue-menu

</style>