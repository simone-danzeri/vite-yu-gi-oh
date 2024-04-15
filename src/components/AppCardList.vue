<script>
import AppEachCard from './AppEachCard.vue';
import { store } from '../store';
    export default {
        name: 'AppCardList',
        components: {
            AppEachCard
        },
        data() {
            return {
                store
            };
        }
    }
</script>


<template>
    <div class="bg-color">
        <div class="card-container">   
            <AppEachCard v-for="eachCard,index in store.yugioh" :key="eachCard.id" :cardInfo="eachCard"></AppEachCard>
        </div>
    </div>
</template>


<style scoped lang="scss">
.bg-color{
    background-color: chocolate;

    .card-container{
        width: 70%;
        margin: 0 auto;
        background-color: aqua;
        display: flex;
        flex-wrap: wrap;
        /* DEBUG */
        height: 1500px;
    }
}
</style>