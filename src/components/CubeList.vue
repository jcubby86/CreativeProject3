<template>
<div class="wrapper">
  <div class="cubes">
    <router-link class="cube" v-for="cube in cubes" :key="cube.id" :to="'/cube/' + cube.id" >
      <div class="info">
        <h1>{{cube.name}}</h1>
      </div>
      <div class="image">
        <img :src="'/images/'+cube.image">
      </div>
    </router-link>
  </div>
</div>
</template>

<script>
export default {
  name: 'CubeList',
  props: {
    cubes: Array
  },
  methods: {
  }
}
</script>

<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.cubes {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  margin-bottom: 50px;
}

.cube {
  margin: 10px;
  margin-top: 50px;
  width: 200px;
}

.cube .image {
  display: flex;
  justify-content: center;
  margin-bottom: 5px;
}

.cube .image img {
  border: 2px solid #333;
  height: 200px;
  width: 200px;
  object-fit: cover;
}

.info {
  background: lightblue;
  color: #000;
  padding: 10px 30px;
  height: 40px;
}

.info h1 {
  font-size: 16px;
}

.auto {
  margin-left: auto;
}
</style>