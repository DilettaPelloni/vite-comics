<script>
    export default {
        name: 'AppMain',

    }
</script>

<template>

    <main>
        <div class="container">
            <div class="content">
                <h2>
                    --> Content goes here &lt--
                </h2>
            </div>
        </div>
    </main>

</template>

<style lang="scss" scoped>
    @import "../style/partials/colors.scss";

    main {
        background-color: $nq-black;
        .content {
            padding: 3rem 0;
            color: white;
            h2 {
                font-size: 2rem;
            }
        }
    }
</style>