<script>
import {store} from './store'


export default {
    data(){
      return{
        store,
      }
    },
    

}
</script>

<template>

  <h1>Tutto collegato </h1>
  <h2>{{store.test}}</h2>
</template>

<style lang="scss">
@use "./assets/style/general.scss" as *;

h1{
  color: red;
}
</style>
