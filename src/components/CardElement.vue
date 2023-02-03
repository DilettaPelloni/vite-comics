
<script>
    export default {
        name: 'CardElement',
        props: {
            label: String,
            src: String,
        },//props
    }
</script>

<template>
    <div>
        <div class="img-box">
            <img :src="src" :alt="label">
        </div>
        <h4>{{ label }}</h4>
        
    </div>
</template>

<style lang="scss" scoped>

    .card {
        margin: 0 1rem 3rem;
        width: 180px;
        .img-box {
            margin-bottom: 1rem;
            aspect-ratio: 1/1;
            overflow: hidden;
            img {
                width: 100%;
            }//img
        }//img-box
        h4 {
            text-transform: uppercase;
            font-weight: 400;
            color: white;
        }
        &:hover h4 {
            text-decoration: underline;
        }
    }//card
</style>