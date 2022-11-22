<script>
import {store} from '../store'
import AppMainTopHalf from './AppMainTopHalf.vue';
import AppMainBotHalf from './AppMainBotHalf.vue';
export default{
    name: "AppMain",
    
    components: {
        AppMainTopHalf,
        AppMainBotHalf,
    },
    data(){
      return{
        store,
      }
    },
  
}

</script>

<template>
<AppMainTopHalf />
<AppMainBotHalf :number="store.number" :mail="store.mail" :gps="store.gps" />


</template>


<style lang="scss">

</style>