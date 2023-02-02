<script>
    export default {
        name: 'AppHeader',
        data() {
            return {
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
                    <li v-for="navitem in navbar">
                        <a :href="navitem.link"> {{ navitem.title }} </a>
                    </li>
                </ul>
            </div><!-- CHIUSUR NAVBAR  -->
        </div><!-- CHIUSUR CONTAINER  -->
    </header>

</template>

<style lang="scss" scoped>

    header {
        .container {
            display: flex;
            justify-content: space-between;

            ul {
                list-style: none;
                display: flex;

                li {

                    a {
                        display: inline-block;
                        padding: 0.5rem 1rem;
                        text-decoration: none;
                        background-color: salmon;
                        border: 1px solid black;
                    }
                }
            }
        }
    }

</style>