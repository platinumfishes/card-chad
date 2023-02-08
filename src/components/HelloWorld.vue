<template>
<!-- Allen's buttons-->
<div class="topbuttons">
  <button id="Duplicate">New duplicate</button>
  <button id="Color">Toggle color</button>
  <button id="Header">Change heading</button>
  <button id="Delete">Delete 1 card</button>
</div>
<!-- Allen's Card-->
  <div id="card1" class="card">
  <p id="header1" class="header">Team Fortress 2 Pyroland</p>
  <p id="bod1" class="bod">This is a screenshot from a 3D rendered animation posted to Youtube by Valve Corporation to promote the video-game Team Fortress 2</p>
  <p id="bod2" class="bod">The video is called "Meet the Pyro"</p>
  <img class="img" src="https://images.gamebanana.com/img/ss/mods/54f8f277e231a.webp" alt="">
  <button id="Details" class="button">Details</button>
  </div>
<!-- End of Allen's cards-->
</template>

<script setup>
import { defineProps, reactive } from 'vue'

defineProps({
  msg: String
})

const state = reactive({ count: 0 })
</script>

<script>

document.querySelector('#Duplicate').addEventListener('click', function() {
  const node1 = document.getElementById("card1");
  let node2 = node1.cloneNode(true);                             
  document.body.appendChild(node2);         
});
 
document.querySelector('#Color').addEventListener('click', function() {
  if (document.getElementById("card1").className == "card")
    document.getElementById("card1").className = "alt";
  else
    document.getElementById("card1").className = "card";
});

document.querySelector('#Header').onclick = function() {
  if (document.getElementById('header1').innerHTML == 'Team Fortress 2 Pyroland')
    document.getElementById('header1').innerHTML = 'Sussy amogus';
  else
    document.getElementById('header1').innerHTML = 'Team Fortress 2 Pyroland';
};

document.querySelector('#Delete').addEventListener('click', function() {
  const list1 = [];
  var onetime = false;
  document.querySelectorAll('.card').forEach((item, index) => {
    list1.push(index);
    if (list1.length != 1 && onetime === false) {
      item.remove();
      onetime = true;
    }
  });
});


document.querySelector('#Details').addEventListener('click', function() {
  if (document.getElementById('bod1').style.visibility == 'hidden') 
  {
    document.getElementById('bod1').style.visibility = 'visible';
    document.getElementById('bod2').style.visibility = 'visible'; 
  }
  else
    {
    document.getElementById('bod1').style.visibility = 'hidden';
    document.getElementById('bod2').style.visibility = 'hidden'; 
    }
});

</script>

<style scoped>
a {
  color: #42b983;
}
</style>
