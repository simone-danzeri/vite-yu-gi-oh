<script>
import axios from 'axios';
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue';
import AppFilter from './components/AppFilter.vue';
import AppCardList from './components/AppCardList.vue';
import AppResultsNumber from './components/AppResultsNumber.vue';

export default {
  components: {
    AppHeader,
    AppFilter,
    AppCardList,
    AppResultsNumber
  },
  data() {
    return {
      store,
/*       myParams: {
        num: 20,
        offset: 0
      } */
    };
  },
  methods: {
    getYugiohInfoFromApi() {
      const myParams = {
        num: 20,
        offset: 0
      }
      if(store.searchedArchetype !== '') {
        myParams.archetype = store.searchedArchetype;
      }
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php', {
        params: myParams
      })
      .then((response) => {
        store.yugioh = response.data.data;
        // console.log(store.yugioh);
      });
    }
  },
  mounted() {
    this.getYugiohInfoFromApi();
  }
}
</script>

<template>
  <AppHeader></AppHeader>

  <main>
    <AppFilter @performedFilter="getYugiohInfoFromApi"></AppFilter>
    <AppCardList></AppCardList>
  </main>
  <AppResultsNumber></AppResultsNumber>
</template>

<style lang="scss">
@use "./style/generic";
.container{
  width: 70%;
  margin: 0 auto;
}
</style>
