<script setup>

const images = [
  {
    title: 'one',
    imageUrl: '/img/img.png'
  },
  {
    title: 'two',
    imageUrl: '/img/img_1.png'
  },
  {
    title: 'three',
    imageUrl: '/img/img_2.png'
  }
]

</script>

<template>
  <div class="container mt-2">
    <h1 class="text-center">Assignment: Vue.js 3 Image Carousel</h1>
    <div class="row">
      <div id="myCarousel" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-inner">
          <div v-for="(image,index) in images" class="carousel-item" :class="0 == index ? 'active' : ''">
            <img :src="image.imageUrl" class="img-fluid" :alt="image.title">
          </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#myCarousel" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#myCarousel" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.carousel-item img {
  height: 700px;
  width: 100%;
}
</style>
