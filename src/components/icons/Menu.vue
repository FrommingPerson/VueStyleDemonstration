<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
  <menu>
    <h3 content="array" class="menu-element">Of style</h3>
    <h3 class="menu-element">0f l0g1cal</h3>
    <h3 class="menu-element">Of Vue</h3>
    <h3 class="menu-element">{{ array[1] }}</h3>
    <!--    <hr class="hr">-->
  </menu>
</template>


<style scoped>

   /*header {
     line-height: 1.5;
   }*/


menu {
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

</style>