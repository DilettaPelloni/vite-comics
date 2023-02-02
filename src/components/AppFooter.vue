<script>
    export default {
        name: 'AppFooter',
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
                dcComicsContent: [
                    {
                        title:'characters',
                        link: '#',
                    },
                    {
                        title:'comics',
                        link: '#',
                    },
                    {
                        title:'Movies',
                        link: '#',
                    },
                    {
                        title:'TV',
                        link: '#',
                    },
                    {
                        title:'games',
                        link: '#',
                    },
                    {
                        title:'videos',
                        link: '#',
                    },
                    {
                        title:'news',
                        link: '#',
                    },
                ],//dcComicsContent
                shopContent: [
                    {
                        title:'shop DC',
                        link: '#',
                    },
                    {
                        title:'shop collectibles',
                        link: '#',
                    },
                ],//shopContent
                dcContent: [
                    {
                        title:'terms of use',
                        link: '#',
                    },
                    {
                        title:'privacy policy (new)',
                        link: '#',
                    },
                    {
                        title:'ad choices',
                        link: '#',
                    },
                    {
                        title:'advertising',
                        link: '#',
                    },
                    {
                        title:'jobs',
                        link: '#',
                    },
                    {
                        title:'subscriptions',
                        link: '#',
                    },
                    {
                        title:'talent workshop',
                        link: '#',
                    },
                    {
                        title:'CPSC certificates',
                        link: '#',
                    },
                    {
                        title:'ratings',
                        link: '#',
                    },
                    {
                        title:'shop help',
                        link: '#',
                    },
                    {
                        title:'contact us',
                        link: '#',
                    },
                ],//dcContent
                sitesContent: [
                    {
                        title:'DC',
                        link: '#',
                    },
                    {
                        title:'MAD magazine',
                        link: '#',
                    },
                    {
                        title:'DC kids',
                        link: '#',
                    },
                    {
                        title:'DC universe',
                        link: '#',
                    },
                    {
                        title:'DC power visa',
                        link: '#',
                    },
                ],//sitesContent
                socialList: [
                    {
                        img: 'footer-facebook.png',
                        link: '#',
                        social: 'facebook',
                    },
                    {
                        img: 'footer-twitter.png',
                        link: '#',
                        social: 'twitter',
                    },
                    {
                        img: 'footer-youtube.png',
                        link: '#',
                        social: 'youtube',
                    },
                    {
                        img: 'footer-pinterest.png',
                        link: '#',
                        social: 'pinterest',
                    },
                    {
                        img: 'footer-periscope.png',
                        link: '#',
                        social: 'periscope',
                    },
                ],//socialList
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

    <footer>

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

        <div class="navlist">
            <div class="container">
                <nav>
                    <div class="col">
                        <div class="list">
                            <h3>DC COMICS</h3>
                            <ul>
                                <li v-for="item in dcComicsContent">
                                    <a :href="item.link"> {{ item.title }} </a>
                                </li>
                            </ul>
                        </div>
                        <div class="list">
                            <h3>SHOP</h3>
                            <ul>
                                <li v-for="item in shopContent">
                                    <a :href="item.link"> {{ item.title }} </a>
                                </li>
                            </ul>
                        </div>
                    </div><!-- CHIUSURA COL1 -->
                    <div class="col">
                        <h3>DC</h3>
                        <ul>
                            <li v-for="item in dcContent">
                                <a :href="item.link"> {{ item.title }} </a>
                            </li>
                        </ul>
                    </div><!-- CHIUSURA COL2 -->
                    <div class="col">
                        <h3>SITES</h3>
                        <ul>
                            <li v-for="item in sitesContent">
                                <a :href="item.link"> {{ item.title }} </a>
                            </li>
                        </ul>
                    </div><!-- CHIUSURA COL3 -->
                </nav>
                <div class="logo-box"></div>
            </div><!-- CHIUSURA CONTAINER -->
        </div><!-- CHIUSURA NAV-LIST -->

        <div class="social-bar">
            <div class="container">
                <a class="button" href="#">sign-up now!</a>

                <div class="social-box">
                    <span>FOLLOW US</span>
                    <a v-for="item in socialList" :href="item.link">
                        <img :src="getImgPath(item.img)" :alt="item.social">
                    </a>
                </div>
            </div><!-- CHIUSURA CONTAINER -->
        </div><!-- CHIUSURA SOCIAL-BAR -->

    </footer>

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

    .navlist {
        background-color: $nq-black;
        background-image: url('../assets/img/footer-bg.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        .container {
            display: flex;
            justify-content: space-between;
            nav {
                padding: 2.5rem 0;
                color: white;
                display: flex;
                .col {
                    margin-right: 2rem;
                    h3 {
                        margin-bottom: 0.4rem;
                    }
                    ul {
                        margin-bottom: 1.2rem;
                        list-style: none;
                        a {
                            color: $light-gray;
                            font-size: 0.8rem;
                            text-transform: capitalize;
                            &:hover {
                                text-decoration: underline;
                            }//a hover
                        }//a
                    }//ul
                }//col
            }//nav
            .logo-box {
                width: 50%;
                background-image: url('../assets/img/dc-logo-bg.png');
                background-repeat: no-repeat;
                background-size: auto 150% ;
                background-position: center;
            }//logo box
        }//container
    }//navlist

    .social-bar {
        padding: 2rem ;
        background-color: $dark-gray;
        .container {
            display: flex;
            justify-content: space-between;
            .social-box {
                display: flex;
                align-items: center;
                span {
                    margin-right: 1rem;
                    color: $dc-blue;
                    font-weight: bold;
                    font-size: 1.5rem;
                }//span
                a {
                    margin-left: 1rem;
                }//a
            }//social box
        }//container
    }//social bar

</style>