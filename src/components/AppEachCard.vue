<script>
    export default {
        name: 'AppEachCard',
        props: {
            cardInfo: Object
        }
    }
</script>


<template>
        <div class="single-card">
        <div class="image">
            <img :src="cardInfo.card_images.image_url" alt="">
        </div>

        <h2>{{ cardInfo.name }}</h2>
        <div>{{ cardInfo.archetype }}</div>
    </div>
</template>


<style scoped lang="scss">
.single-card {
    width: calc((100% / 5) - 10px);
    text-align: center;
    margin: 10px 5px;

    .image {
        img {
            width: 100%;
        }
    }
}
</style>