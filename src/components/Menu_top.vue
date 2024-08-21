<script setup>
</script>

<template>
  <menu>
  <nav>


<!--        <a href="#style">style</a>
        <a href="#logical">logical</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
        <a href="#gallery">Gallery</a>-->
    <a href="#style"  class="menu-element">Of style</a>
    <a href="#logical"  class="menu-element">0f l0g1cal</a>
    <a href="#vue" class="menu-element">Of Vue</a>
    <SearchBar v-model="searchQuery" />
  </nav>

  </menu>

</template>

<style scoped>
menu {
  padding: 5px;
  position: fixed;
  top: 15px;
  z-index: 7;
  backdrop-filter: blur(2px);
  border: #f8f8f8 solid;
  border-radius: 20px;
}
.menu-element {
  display: inline-block;
  margin-left: 25px;
  font-family: "Al Nile", sans-serif;
  font-size: 26px;
  color: #2c3e50;
  font-weight: bolder;
  cursor: pointer;
  -webkit-user-select: none;
  text-shadow: aliceblue 1px 1px 3px;
  /* user-select -- это нестандартное свойство */
  -moz-user-select: none;
  /* поэтому нужны префиксы */
  -ms-user-select: none;
}
.menu-element:hover {
  text-shadow: hsla(160, 100%, 37%, 1) 1px 1px 3px;
}
.menu-element:active {
  transform: translateY(-1.3px);
}
.menu-element:hover::after {
  transform: scaleX(1.2) scaleY(1.4);
  opacity: 0;
}
.menu-actived {
  background-color: hsla(160, 100%, 37%, 1);
}

a:hover {
  background: none;
}
</style>