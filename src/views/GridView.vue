<template>
  <div class="container">
    <img class="image1" src="https://images.unsplash.com/photo-1657664049360-66ca933f7a82?ixlib=rb-1.2.1&ixid=MnwxMjA3fDF8MHxlZGl0b3JpYWwtZmVlZHwxfHx8ZW58MHx8fHw%3D&auto=format&fit=crop&w=500&q=60" alt="">
    <img class="image2" src="https://images.unsplash.com/photo-1662763998553-0b6c226e305c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwyfHx8ZW58MHx8fHw%3D&auto=format&fit=crop&w=500&q=60" alt="">
    <img class="image3" src="https://images.unsplash.com/photo-1662751886847-74b4f8bd5a9b?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwzfHx8ZW58MHx8fHw%3D&auto=format&fit=crop&w=500&q=60" alt="">
    <img class="image4" src="https://images.unsplash.com/photo-1662756069030-280fe04ca0ed?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHw4fHx8ZW58MHx8fHw%3D&auto=format&fit=crop&w=500&q=60" alt="">
    <img class="image5" src="https://images.unsplash.com/photo-1662751577063-0f4c15d73a4d?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwxN3x8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=60" alt="">
    <img class="image6" src="https://images.unsplash.com/photo-1662755674873-c3311e6e4086?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwyNHx8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=60" alt="">
    <img class="image7" src="https://images.unsplash.com/photo-1662893236984-6d806c610a78?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwyOHx8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=60" alt="">
    <img class="image8" src="https://images.unsplash.com/photo-1662864897562-2bc68e82859a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHw0M3x8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=60" alt="">
    <img class="image9" src="https://images.unsplash.com/photo-1662867991504-44e03c104ac8?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHw0N3x8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=60" alt="">
    <img class="image10" src="https://images.unsplash.com/photo-1662829197387-b243c7849743?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHw1NXx8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=60" alt="">
  </div> 
</template>

<script>
export default {

}
</script>

<style>
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;
  grid-gap: 1rem;
  grid-template-areas: 
  'a a a'
  'b b c'
  'b b d'
  'e e e'
  'f f g'
  'h i j'
  'h i j';
}
.container img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.image1 {
  grid-area: a;
}
.image2 {
  grid-area: b;
}
.image3 {
  grid-area: c;
}
.image4 {
  grid-area: d;
}
.image5 {
  grid-area: e;
}
.image6 {
  grid-area: f;
}
.image7 {
  grid-area: g;
}
.image8 {
  grid-area: h;
}
.image9 {
  grid-area: i;
}
.image10 {
  grid-area: j;
}

</style>