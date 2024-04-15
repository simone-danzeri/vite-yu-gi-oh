<script>
    export default {
        name: 'AppEachCard'
    }
</script>


<template>
        <div class="single-card">
        <div class="image">
            <img src="" alt="">
        </div>

        <h2>[titolo]</h2>
        <div>[Archetipo]</div>
    </div>
</template>


<style scoped lang="scss">
.character-card {
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