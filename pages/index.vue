<template>
  <div>
    <div v-for="home in homes" :key="home.objectID">
    <img :src='home.images[0]' style="width:200px"><br>
    {{ home.title}}<br>
    </div>
  </div>
</template>
<script>
import { once } from 'events'
import homes from '../data/homes.json'

export default {
  data(){
    return {
      homes: homes.slice(0,3)
    }
  }
}
</script>