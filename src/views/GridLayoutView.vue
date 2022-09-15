<template>
  <div class="container">
    <header class="header">header</header>
    <main class="main">main</main>
    <aside class="aside">aside</aside>
    <footer class="footer">footer</footer>
  </div>  
</template>

<script>
export default {

}
</script>

<style>
.container {
  width: 100vw;
  height: 100vh;
  display: grid;
  grid-template-columns: 3fr 1fr;
  grid-auto-rows: 100px auto 50px;
  grid-gap: 1rem;
  grid-template-areas: 
    'header header'
    'main aside'
    'footer footer'
  ;
}

.header {
  grid-area: header;
}
.main {
  grid-area: main;
}
.aside {
  grid-area: aside;
}
.footer {
  grid-area: footer;
}
</style>