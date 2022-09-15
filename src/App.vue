<template>
  <nav class="fix-nav">
    <router-link to="/">H</router-link>
    <router-link to="/about">A</router-link>
    <router-link to="/grid">G</router-link>
    <router-link to="/gridLayout">R</router-link>
    <router-link to="/bana">B</router-link>
  </nav>
  <router-view class="view" />
</template>

<style lang="scss">
body, html {
  margin: 0;
  padding: 0;
  overflow: hidden;
}


#app {
  width: 100vw;
  height: 100vh;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

  display: grid;
  grid-template-rows: 100%;
  grid-template-columns: 50px auto;
  grid-template-areas: 
  'nav view view view'
  ;
}
.fix-nav {
  grid-area: nav;
  display: grid;
  grid-template-columns: 50px;
  // grid-template-rows: 50px / 50px;
  grid-auto-rows: 50px;
  width: 50px;
  background: #dfdfdf;
  a {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 50px;
    height: 50px;
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
.view {
  grid-area: view;
}

@media screen and (max-width: 640px) {
  #app {
    grid-template-columns: 0 auto;
    grid-template-areas: 
    'nav view view view'
    ;
  }
}
</style>
