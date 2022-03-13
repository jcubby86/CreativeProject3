<template>
  <div class="about">
    <h1>About My Collection</h1>
    <div class="image">
        <img :src="'/images/stand.jpg'">
      </div>
    <p>
      I started getting interested in Rubik's cubes when I was in the 9th grade. I had a friend that lent me their cube so I could figure out how to solve it, and I watched a video tutorial to learn the steps.
      The first time I solved a 3x3 cube without the help of a video (but still using the written algorithms) it took me nearly 20 minutes. At my best, I was able to solve the cube in less than a minute.
    </p>
    <p>
      After I had been having fun with the 3x3 for a long time, I wanted to try something different, so I purchased a set that had a 2x2, 4x4 and 5x5 cubes in it. 
      The bigger cubes especially were quite fun to learn new algorithms and techniques to be able to solve. Since then, my collection has continued expanding mostly through gifts from others -
      and I make an occasional purchase myself.
    </p>
  </div>
</template>

<style scoped>
h1 {
  text-decoration: underline;
}
p {
  max-width: 1000px;
  margin: 10px auto;
}

.image img {
  border: 2px solid #333;
  max-width: 100%;
  object-fit: cover;
}

.about {
  margin-bottom: 50px;
}

@media only screen and (min-width: 500px) {
  .image img {
    height: 500px;
    width: 500px;
    object-fit: cover;
  }
}

</style>