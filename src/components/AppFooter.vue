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
                            <h4>DC COMICS</h4>
                            <ul>
                                <li v-for="item in dcComicsContent">
                                    <a :href="item.link"> {{ item.title }} </a>
                                </li>
                            </ul>
                        </div>
                        <div class="list">
                            <h4>SHOP</h4>
                            <ul>
                                <li v-for="item in shopContent">
                                    <a :href="item.link"> {{ item.title }} </a>
                                </li>
                            </ul>
                        </div>
                    </div><!-- CHIUSURA COL1 -->
                    <div class="col">
                        <h4>DC</h4>
                        <ul>
                            <li v-for="item in dcContent">
                                <a :href="item.link"> {{ item.title }} </a>
                            </li>
                        </ul>
                    </div><!-- CHIUSURA COL2 -->
                    <div class="col">
                        <h4>SITES</h4>
                        <ul>
                            <li v-for="item in sitesContent">
                                <a :href="item.link"> {{ item.title }} </a>
                            </li>
                        </ul>
                    </div><!-- CHIUSURA COL3 -->
                </nav>
                <div class="logo-box">
                    <img src="../assets/img/dc-logo-bg.png" alt="dc-logo-bg">
                </div><!-- CHIUSURA LOGO-BOX -->
            </div><!-- CHIUSURA CONTAINER -->
        </div><!-- CHIUSURA NAV-LIST -->

        <div class="social-bar">
            <div class="container">

            </div><!-- CHIUSURA CONTAINER -->
        </div><!-- CHIUSURA SOCIAL-BAR -->

    </footer>

</template>

<style lang="scss" scoped>
    .blue-menu {
        background-color: #0880f8;
        ul {
            list-style: none;
            display: flex;
        }//ul
    }//blue-menu

    .navlist {
        .container {
            display: flex;
            justify-content: space-between;
            nav {
                display: flex;
                ul {
                    list-style: none;
                }
            }//nav
        }//container
    }//navlist


</style>