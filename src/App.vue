<script setup>
import Menu_top from "@/components/Menu_top.vue";
import LogicalMoment from "@/components/LogicalMoment.vue";
import OfVue from "@/components/OfVue.vue";

function changeClass(element_id, toggle_class, element_idOfBut = "", toggle_classOfBut = "") {
  const el = document.querySelector(`#${element_id}`);
  el.classList.toggle(toggle_class);
  const el2 = document.querySelector(`#${element_idOfBut}`);
  el2.classList.toggle(toggle_classOfBut);
}

const sections = document.querySelectorAll("section[id]");

// Add an event listener listening for scroll
// window.addEventListener("scroll", );
</script>

<template>
  <Menu_top/>

  <header>
      <div class="content">
        <div class="epic">
    <section id="style">
      <h1 class="h1">Of style</h1>
          <div class="">
            <div class="buttons">
              <button class="selector" v-on:click="changeClass('one', 'animatedIn')">The animation of "in" type </button>
              <button class="selector" v-on:click="changeClass('two', 'animatedOut')">The animation of "out" type</button>
              <button id="infinity" class="selector"
                 v-on:click="changeClass('three', 'animated', 'infinity', 'selector-active')">The animation of
                "infinite"
                type</button>
            </div>
            <hr>
            <div class="examples">
              <div id="one" class="example-animation"></div>
              <div id="two" class="example-animation"></div>
              <div id="three" class="example-animation"></div>
            </div>
          </div>

          <div class="text">
            <h1>About difference between those type of animation🎨</h1>
            <div class="text-field">
              <p class="about">Based on that what you saw, I can explain easily how this is happening. What is about the
                IN animation? — I don't know! What is about the OUT animation? — I don't know! Whats about is the
                infinite animation? — It has infinity!</p>
            </div>
            <h1 class="title">Next chapter>>></h1>
            <div class="text-field">
              <p class="about">What do you know of text? For example in this part of interactive article I goona tell
                about text-formation and another styles&</p>
            </div>
          </div>

          <div class="buttons2" style="--second:true">
            <button id="bend" class="selector" v-on:click="changeClass('texting','bending-text', 'bend', 'selector-active')">
              Bending style of font</button>
            <button id="top" class="selector" v-on:click="changeClass('texting','top-font', 'top', 'selector-active')">The
              font
              is American Typewriter</button>
            <button id="shadow" class="selector"
               v-on:click="changeClass('texting', 'super-style', 'shadow', 'selector-active')">Super text shadow</button>
          </div>
          <div class="text">
            <div class="text-field">
              <p id="texting" class="text-example">What do we know about a lark or amusement? These oafs do us very
                sensitive and we are quite excited of it also we've been thinking of these arrogant snorts</p>
            </div>

          </div>
    </section>

    <section id="logical">
          <div class="text-field2">
<!--            <div>-->
      <LogicalMoment/>
<!--            </div>-->
          </div>
    </section>

          <section id="vue">
            <div class="text-field2">
              <OfVue/>
            </div>
          </section>

        </div>
      </div>
  </header>

</template>

<style scoped>

.h1 {
  position: relative;
//top: -25px;
  font-size: 42px;
  font-family: Baghdad;
}

.examples {
  position: relative;
  top: 10px;
  flex-wrap: wrap;
  display: flex;
  justify-content: center;
  align-items: center;
}

.buttons2 {
  position: relative;
  top: 17px;
  flex-wrap: wrap;
  display: flex;
  justify-content: center;
  align-items: center;
  /*display: flex; justify-content: center; align-items: center;*/
}

.selector {
  padding: 5px;
  display: inline-block;
  font-family: Baghdad, sans-serif;
  font-size: 15px;
  color: hsla(160, 100%, 37%, 1);
  margin-left: 20px;
  background: #383737;
  border-radius: 12px;
  box-shadow: 1px 1px 3px rgb(126, 122, 122);
  -webkit-user-select: none;
  /* user-select -- это нестандартное свойство */
  -moz-user-select: none;
  /* поэтому нужны префиксы */
  -ms-user-select: none;
}

.selector:hover {
  color: #ffffff;
  background-color: hsla(160, 100%, 37%, 1);
  box-shadow: 3px 3px 3px rgb(126, 122, 122);
}

.selector:active {
  transform: translateY(-1.3px);
}

.selector:hover::after {
  transform: scaleX(1.2) scaleY(1.4);
  opacity: 0;
}

.example-animation {
  display: inline-block;
  margin-top: 15px;
  margin-left: 20px;
  background-color: #613de3;
  width: 10vmax;
  height: 10vmax;
  border-radius: 15px;
  border: hsla(160, 100%, 37%, 1) 13px dashed;
  box-shadow: 3px 3px 3px rgb(126, 122, 122);
}

header {
  display: flex;
  place-items: center;
  padding-right: calc(var(--section-gap) / 2);
}

@media (min-width: 24px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    position: relative;
  //margin: 0 2rem 0 0;
  }
}

/*Additional classes os ids*/

.bending-text {
  writing-mode: vertical-rl;
}

.top-font {
  font-family: "American Typewriter", Sathu;
}

.super-style {
  text-shadow: #613de3 2px 1px 3px;
}

.selector-active {
  color: #2c3e50;
  background-color: hsla(160, 100%, 37%, 1);
//box-shadow: 3px 3px 3px rgb(126, 122, 122);
}

/*ANIMATION PART*/
.animatedIn {
  animation: ease-in 2s show;
}

.animatedOut {
  animation: ease-out 2s show;
}

.animated {
  animation: infinite 2s show;
}

@keyframes show {
  from {
    opacity: 0;
    box-shadow: 07px 07px 07px rgb(126, 122, 122);
    transform: scaleX(0.7);
    transform: scaleY(0.9);
  }
  to {
    opacity: 1;
    box-shadow: 3px 3px 3px rgb(126, 122, 122);
    transform: scaleX(1);
    transform: scaleY(1);
  }
}
</style>
