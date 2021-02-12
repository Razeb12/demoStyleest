<template>
  <div>
    <h1 class="title">Lorem ipsum dolor sit amet.</h1>
    <div class="container-fluid">
      <div class="gallery">
        <figure class="gallery__item gallery__item--1">
          <img
            src="../assets/grid_1.jpg"
            alt="Gallery image 1"
            class="gallery__img"
          />
        </figure>
        <figure class="gallery__item gallery__item--2">
          <img
            src="../assets/grid_2.jpg"
            alt="Gallery image 2"
            class="gallery__img"
          />
        </figure>
        <figure class="gallery__item gallery__item--3">
          <img
            src="../assets/grid_3.jpg"
            alt="Gallery image 3"
            class="gallery__img"
          />
        </figure>
        <figure class="gallery__item gallery__item--4">
          <img
            src="../assets/grid_4.jpg"
            alt="Gallery image 4"
            class="gallery__img"
          />
        </figure>
        <figure class="gallery__item gallery__item--5">
          <img
            src="../assets/cat1.jpg"
            alt="Gallery image 5"
            class="gallery__img"
          />
        </figure>
        <figure class="gallery__item gallery__item--6">
          <img
            src="../assets/cat3.jpg"
            alt="Gallery image 6"
            class="gallery__img"
          />
        </figure>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ImageGallery",
};
</script>

<style scoped>
.container {
  width: 100%;
  margin: 2rem auto; 
}

.gallery {
  display: grid;
  grid-template-columns: repeat(8, 1fr);
  grid-template-rows: repeat(8, 5vw);
  grid-gap: 1.5rem; 
}

.gallery__img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block; 
}

.gallery__item--1 {
  grid-column-start: 1;
  grid-column-end: 3;
  grid-row-start: 1;
  grid-row-end: 3;
}

.gallery__item--2 {
  grid-column-start: 3;
  grid-column-end: 5;
  grid-row-start: 1;
  grid-row-end: 3;
}

.gallery__item--3 {
  grid-column-start: 5;
  grid-column-end: 7;
  grid-row-start: 1;
  grid-row-end: 3;
}
.gallery__item--4 {
  grid-column-start: 7;
  grid-column-end: 9;
  grid-row-start: 1;
  grid-row-end: 3;
}
.gallery__item--3 {
  grid-column-start: 5;
  grid-column-end: 7;
  grid-row-start: 1;
  grid-row-end: 3;
}

.title {
  text-align: center;
}
</style>