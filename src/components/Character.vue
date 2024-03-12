<script setup>
import CharacterImage from './../assets/character.png'
</script>

<template>
    <div class="character">
      <img :src=CharacterImage>
    </div>
</template>

<style>
@keyframes sizein {
 to {
    transform: translateX(-50%) scale(1);
 }   
}

.character {
    position: absolute;
    top: 2%;
    left: 55%;
    transform: translateX(-50%) scale(.8);
    transform-origin: center bottom;
    animation-duration: 1s;
    animation-name: sizein;
    animation-timing-function: cubic-bezier(.7,0,.3,1);
    animation-fill-mode: forwards;
}

.character > img {
  height: 110vh;
}
</style>