<template>
  <div id="nav">
    <router-link to="/">hjem</router-link> |
    <router-link to="/om">om</router-link> |
    <router-link to="/hjelp">hjelp</router-link>
  </div>
  <router-view />
</template>

<style>
body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  background-color: rgb(18, 42, 51);
  color: white
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: rgb(0, 187, 255);
}

#nav a.router-link-exact-active {
  color: white
}

</style>
