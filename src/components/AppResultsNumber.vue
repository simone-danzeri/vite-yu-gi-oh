<script>
    import { store} from '../store'
    export default {
        name: 'AppResultsNumber',
        data() {
            return {
                store
            };
        }
    }
</script>


<template>
    <div class="container">
        <span>Ho trovato {{ store.yugioh.length }} carte con l'archetipo {{ store.searchedArchetype }}</span>
    </div>
</template>


<style scoped lang="scss">
.container{
    text-align: center;
    padding: 40px 0;

    span{
        font-size: 40px;
    }
}
</style>