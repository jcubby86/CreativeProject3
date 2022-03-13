<template>
  <div class="home">
    <h1>My Rubik's Cube Collection</h1>
    <CubeList :cubes="cubes"/>
  </div>
</template>

<script>
// @ is an alias to /src
import CubeList from '@/components/CubeList.vue'

export default {
  name: 'HomeView',
  components: {
    CubeList
  },
  computed: {
    cubes() {
      return this.$root.$data.cubes;
    }
  },
}
</script>

<style scoped>
.home h1 {
  text-decoration: underline;
}
</style>
