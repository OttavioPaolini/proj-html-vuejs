<script>
import {store} from './store'

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  components:{
    AppHeader,
    AppMain,
    AppFooter,
  },
    data(){
      return{
        store,
      }
    },
    

}
</script>

<template>
<header>
<AppHeader  :number="store.number" :mail="store.mail" :gps="store.gps"/>
</header>

<main>
<AppMain />
</main>

<footer>
<AppFooter :number="store.number" :mail="store.mail" :gps="store.gps"/>
</footer>
  
</template>

<style lang="scss">
@use "./assets/style/general.scss" as *;
@use "./assets/style/partials/variables" as *;



</style>
