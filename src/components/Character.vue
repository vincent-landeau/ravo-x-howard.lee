<script setup>
import CharacterImage from './../assets/character.png'
</script>

<template>
    <div class="character animated">
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
    left: 54%;
    transform: translateX(-50%) scale(.8);
    transform-origin: center bottom;
    animation-name: sizein;
}

.character > img {
  height: 110vh;
}
</style>