<template>
<div>
  <div class="info">
    <h1>{{cube.name}}</h1>
    <img :src="'/images/'+cube.image">
    <p> {{cube.description}} </p>
  </div>
  <div class="related" v-show="cube.related.length>0">
    <h2>Related Cubes</h2>
    <CubeList :cubes="relatedCubes"/>
  </div>
</div>
</template>

<script>
import CubeList from '@/components/CubeList.vue'
export default {
  name: 'CubeView',
  components: {
    CubeList
  },
  data() {
    return {
      cube: {},
    }
  },
  computed: {
    relatedCubes() {
      return this.$root.$data.cubes.filter(c => this.cube.related.includes(c.id))
    }
  },
  created() {
    this.cube = this.$root.$data.cubes.find(cube => cube.id === parseInt(this.$route.params.id));
  },
  watch: {
    "$route.params.id"(val) {
      this.cube = this.$root.$data.cubes.find(cube => cube.id === parseInt(val));
    },
  }
}
</script>

<style scoped>

.info img {
  border: 1px solid #333;
  width: 100%;
  object-fit: cover;
}

.info {
  margin: 0 10px 50px;
}

.related h2 {
  margin-bottom: 0;
  text-decoration: underline;
}

@media only screen and (min-width: 500px) {
  .info img {
    height: 500px;
    width: 500px;
    object-fit: cover;
  }
}
</style>
