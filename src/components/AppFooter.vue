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

            </div>

        </div>

        <div class="navlist">

            <div class="container">

            </div>

        </div>

        <div class="social-bar">

            <div class="container">

            </div>

        </div>

    </footer>

</template>

<style lang="scss" scoped>

    .blue-menu {
        background-color: #0880f8;

        ul {
            list-style: none;
            display: flex;
        }
    }


</style>