<script>
    import axios from 'axios';
import { store} from '../store'
    export default {
        name: 'AppFilter',
        data() {
            return {
                store,
                availableArchetypes: []
            };
        },
        methods: {
            getArchetypesFromAPI() {
                axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
                .then((response) => {
                    // console.log(response);
                    this.availableArchetypes.push(response.data);
                    console.log(this.availableArchetypes);
                });

            }
        },
        mounted() {
            this.getArchetypesFromAPI();
        }
    }
</script>


<template>
    <div class="container">
        <select>
            <!-- Option di base -->
            <option value="">Scegli un archetipo</option>
            <!-- Option da scegliere -->
            <option v-for="eachArchetype in availableArchetypes[0]" :value="eachArchetype.archetype_name">{{ eachArchetype.archetype_name }}</option>
        </select>
    </div>
</template>


<style scoped lang="scss">
.container{
    padding-top: 20px;
}
</style>