<script>
import axios from 'axios';
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue';
import AppCardList from './components/AppCardList.vue';

export default {
  components: {
    AppHeader,
    AppCardList
  }
}

</script>

<template>
<AppHeader></AppHeader>

<main>
<AppCardList></AppCardList>
</main>
</template>

<style lang="scss">
@use './style/generic';
</style>
