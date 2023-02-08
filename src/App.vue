<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3 + Vite" />
</template>

<script setup>
import HelloWorld from './components/HelloWorld.vue'

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.alt {
  width: 500px;
  height: 565px;
  border: 14px solid #72fc79;
  background-color: cyan;
  text-align: center;
  border-radius: 20px;
  margin: auto;
}
.topbuttons {
  display: block;
  margin: auto;
}

button {
  font-size: 24px;
  margin-top: 12px;
  margin-bottom: 12px;
  background-color: #94FEFB;
  font-family: "Monaco", Monospace;
  border: 4px solid pink;
  border-radius: 20px;
}

/*BELOW IS ALL ORIGINAL CARD SPACE*/

.card {
  width: 500px;
  height: 565px;
  border: 14px solid pink;
  background-color: #FB94FE;
  text-align: center;
  border-radius: 20px;
  margin: auto;
}

.header {
  color: #94FEFB;
  font-family: "Lucida Console", monospace;
  font-size: 30px;
  border: 2px solid;
  border-radius: 16px;
  Margin: 16px;
  padding: 8px;
  background-color: #ff66cc;
}

.bod {
  color: blue;
  font-family: "Monaco", Monospace;
  font-size: 20px;
  margin-left: 8px;
  margin-right: 8px;
  visibility: hidden;
}

.img {
  width: 460px;
  height: 250px;
  border: 2px inset #94FEFB;
  padding: 8px;
  background-color: #ff66cc;
  border-radius: 20px;
}

.button {
  background-color: hotpink;
  color: #94FEFB;
  padding: 8px;
  border: 2px dashed #94FEFB;
  font-family: "Monaco", Monospace;
  visibility: hidden;
  border-radius: 24px;
  margin-top: 0px;
  font-size: 20px;
}
.button:hover,
.button:focus,
.topbuttons button:hover,
.topbuttons button:focus {
  color: hotpink;
  background-color: #94FEFB;
}
.button:active,
.topbuttons button:active {
  color: #94FEFB;
  background-color: #ec72fc
}

@media screen and (max-width: 800px) and (min-width: 500px) {
  .button {
    visibility: visible;
  }
}

@media screen and (max-width: 500px) {
  .card {
    width: auto;
    height: auto;
  }
  .img {
    width: 90%;
    height: auto;
  }
  .header{
    font-size: 4vw;
  }
  .bod {
    font-size: 4vw;
  }
}

input:checked + label + .description { display:none; }



</style>
