<template>
  <div>
    <h1>Create an Event</h1>
    <p>This event was created by {{user.name}}</p>
    <p>There are {{catLength}} categories available</p>
    <ul>
      <li v-for="cat in categories" :key="cat">{{ cat }}</li>
    </ul>
  </div>
</template>

<script>
import { mapState } from 'vuex'
  export default {
    computed:{
      catLength() {
        return this.$store.getters.catLength;
      },
      ...mapState(['user','categories'])
    }   
  }
</script>

<style scoped>

</style>