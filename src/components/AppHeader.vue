<script>
    export default {
        name: 'AppHeader',
        data() {
            return {
                active: 0,
                navbar: [
                    {
                        title: 'characters',
                        link: '#',
                    },
                    {
                        title: 'comics',
                        link: '#',
                    },
                    {
                        title: 'movies',
                        link: '#',
                    },
                    {
                        title: 'tv',
                        link: '#',
                    },
                    {
                        title: 'games',
                        link: '#',
                    },
                    {
                        title: 'collectibles',
                        link: '#',
                    },
                    {
                        title: 'videos',
                        link: '#',
                    },
                    {
                        title: 'fans',
                        link: '#',
                    },
                    {
                        title: 'news',
                        link: '#',
                    },
                    {
                        title: 'shop',
                        link: '#',
                    },
                ]//navbar
            } //return
        },//data
    }
</script>

<template>

    <header>
        <div class="container">
            <div class="logo-box">
                <img src="../assets/img/dc-logo.png" alt="dc-logo">
            </div><!-- CHIUSURA LOGO-BOX  -->
            <div class="navbar">
                <ul>
                    <li v-for="navitem, i in navbar">
                        <a
                        :href="navitem.link"
                        @click="active = i"
                        :class="{
                            active: active == i,
                        }">
                            {{ navitem.title }}
                        </a>
                    </li>
                </ul>
            </div><!-- CHIUSUR NAVBAR  -->
        </div><!-- CHIUSUR CONTAINER  -->
    </header>

</template>

<style lang="scss" scoped>

    header {
        background-color: white;
        .container {
            height: 120px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            .logo-box {
                padding: 1rem 0;
                height: 100%;
                img {
                    height: 100%;
                }
            }
            ul {
                list-style: none;
                display: flex;
                a {
                    padding: 0 1rem;
                    display: inline-block;
                    height: 120px;
                    line-height: 120px;
                    font-size: 0.9rem;
                    text-transform: uppercase;
                    font-weight: bold;
                    color: $nq-black;

                    &.active {
                        color: $dc-blue;
                        box-shadow: inset 0px -5px 0px 0px $dc-blue;
                    }
                    &:hover {
                        color: $dc-blue;
                    }
                }//a
            }//ul
        }//container
    }//header

</style>