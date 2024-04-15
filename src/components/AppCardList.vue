<script>
import AppEachCard from './AppEachCard.vue';
    export default {
        name: 'AppCardList',
        components: {
            AppEachCard
        }
    }
</script>


<template>
    <div class="bg-color">
        <section class="card-container">   
            <AppEachCard></AppEachCard>
        </section>
    </div>
</template>


<style scoped lang="scss">
.bg-color{
    background-color: chocolate;

    .card-container{
        width: 70%;
        margin: 0 auto;
        background-color: aqua;
        /* DEBUG */
        height: 1500px;
    }
}
</style>