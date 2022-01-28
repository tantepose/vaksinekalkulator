<template>
  <div id="nav">
    <router-link to="/">kalkulatoren</router-link> |
    <router-link to="/om">om</router-link>
  </div>
  <router-view />
</template>

<style>
body {
  font-family: 'Nixie One', cursive;
  text-align: center;
  background-color: rgb(27, 27, 27);
  color: white
}

p {
  font-size: 1.3em;
}

.big {
  font-size: 10em;
  color: rgb(247, 208, 243);
}

h1 {
  font-size: 2em;
  color: rgb(247, 208, 243);
  margin: 10px;
}

#nav {
  padding: 10px;
}

a, a:visited {
  color: rgb(247, 208, 243);
}

#nav a.router-link-exact-active {
  color: white
}

</style>