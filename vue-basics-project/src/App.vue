<script setup>
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
import MyList from './components/MyList.vue';
import { ref } from 'vue';

const myName = ref('Tobi');
let ifTrue = true;

const getMyName = function() {
  return 'My Name is ' + myName.value;
}

const backgroundColor = ref('#6B708D');
const blueBackground = ref('blue');
const redBackground = ref('red');
const whiteBackground = ref('white');

const setBackgroundColor = (val) => {
  document.querySelector('body').style.backgroundColor = val;
}
</script>

<template>
  <Navbar></Navbar>
  <p>2 + 2</p>
  2 + 2 
  <br>
  {{ 2 + 2 }}
  <br>
  {{ getMyName() }}
  <br>
  <h1 v-if="ifTrue == true">This only shows, if true</h1>
  <br>
  <br>
  <MyList></MyList>
  <br>
  <div>
    <input type="text" v-model="backgroundColor" />
    <button @click="setBackgroundColor(backgroundColor)">
      Change background
    </button>
    <br>
    <button @click="setBackgroundColor(blueBackground)">
      Change background to blue
    </button>
    <br>
    <button @click="setBackgroundColor(redBackground)">
      Change background to red
    </button>
    <br>
    <button @click="setBackgroundColor(whiteBackground)">
      Change background to white
    </button>
  </div>

  <Footer></Footer>
</template>

<style>
</style>