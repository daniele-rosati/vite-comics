<script>
    export default{
        name: "SingleCard",
        props: ["comic"],
    }
</script>

<template>
    <div class="card">
        <div class="img-wrapper">
            <img :src="comic.thumb" alt="">
        </div>
        <div class="title"> {{ comic.series }} </div>
    </div>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;
    
    .card{
        width: calc(100% / 6 - 8px);
        margin: 8px 0;
        .img-wrapper {
            width: 100%;
            aspect-ratio: 1;
            overflow: hidden;
            img {
                width: 100%;
            }
        }
        .title{
            margin-top: 16px;
            text-transform: uppercase;
            font-size: 1rem;
        }
    }
</style>