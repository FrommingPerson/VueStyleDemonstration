<script setup>
function copying(textId) {
  let copyText = document.getElementById(`${textId}`);
  // alert("Copied the text: " + copyText.textContent);
  /*// Get the text field

  // Select the text field
  copyText.select();
  copyText.setSelectionRange(0, 99999); // For mobile devices

  // Copy the text inside the text field
  navigator.clipboard.writeText(copyText.value);

  // Alert the copied text
  */
  navigator.clipboard.writeText(copyText.textContent);
}
</script>

<template>

  <div class="content">
    <div>
      <h1>0f l0g1cal</h1>
      <div class="text-field">
      <p class="about">This article's part tell's you all about logic of programming especially for Java Script. Below you can the various ways realizing
        of algorithm which finds the factorial of any number (<span class="focus-red">number mustn't be more than 300!!!</span>). If we are talking of the
        compiled languages we might not pay much attention on optimization of code, because when compilation takes place at once happening rewriting the code!
        As you've know this fact, now you don't need in super rewriting for optimization of code, better you can pay attention on readability!! But that fact not actual for Java Script.</p>
      </div>
      <div class="text-field">
        <pre id="firstWay" class="code-example">
factorial(100);

function factorial(n) {
    if (n &#x3E; 1 &#x26;&#x26; n &#x3C; 300) {
        console.log((n - 1) * n);
        return factorial((n - 1) * n);
    } else {
        console.log(n);
        return 1;
    }
}</pre>
        <pre id="secondWay" class="code-example">
factorial<span class="focus-green">Remaster</span>(100);

function factorial<span class="focus-green">Remaster</span>(n) {
    let result = 1;
    while (n &#x3E; 1 &#x26;&#x26; n &#x3C; 300) {
        result *= n;
        n -= 1;
    }
    console.log(result);
    return result;
}</pre>
      </div>
      <div class="buttons">
        <button v-on:click="copying('firstWay')"  class="selector">To borrow first way</button>
        <button v-on:click="copying('secondWay')"  class="selector">To borrow second way</button>
      </div>
      <div class="text-field">
      <p class="about">Java Script is a interpreted programming language this fact is mean that clear of code is very matter! For efficiency work the program.</p>
      </div>
    </div>
  </div>

</template>

<style scoped>

h1 {
  position: relative;
//top: -25px;
  font-size: 42px;
  font-family: Baghdad;
}

pre {
//text-align: center;
}

.code-example {
  display: inline-block;
}

.text-field:has(.code-example) {
  //margin-top: 15px;
  padding: 15px;
  background-color: #613de3;
  background-blend-mode: difference;
  color: white;
  text-shadow: #3d3d3d 1px 1px 1px;
  border-radius: 30px;
  margin-top: 85px;
  //position: relative;
  //top: -55px;
  box-shadow: #2c3e50 2px 2px 3px;
}

.focus-green {
  color: chartreuse;
  font-size: 18px;
}

.focus-green:hover {
  color: hsla(160, 100%, 37%, 1);
}

.focus-red {
  color: indianred;
  font-weight: bolder;
}

.focus-red:hover {
  color: orangered;
}

.about {
  margin-top: 15px;
}

</style>