<template>
  <NavbarComp />
  <router-view />
  <FooterComp />
</template>

<script>
import NavbarComp from './components/NavbarComp.vue';
import FooterComp from './components/FooterComp'
export default{
components:{
  NavbarComp,
  FooterComp
}
}
</script>

<style>
body{
background-color: #000000;
font-family:Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
color: #2c3e50;
text-align: center;
}

#app {
-webkit-font-smoothing: antialiased;
-moz-osx-font-smoothing: grayscale;
color: #ffffff;
overflow-x: hidden;
}

nav {
text-align: right;
padding: 30px;
box-shadow: 7px 7px 7px #2c3e50;
}

nav a { 
font-weight: bold;
color: #2c3e50;
padding: 10px;
text-align: right;
}

nav a.router-link-exact-active {
color: #42b983;
}
</style>
