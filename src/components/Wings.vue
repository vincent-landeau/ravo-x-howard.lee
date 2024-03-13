<script setup>
import {WingAbstractIcon} from "./icons/AbstractIcons.js"
</script>

<template>
    <div class="wings-container">
        <div class="wings animated">
          <WingAbstractIcon class="wing animated"/>
          <WingAbstractIcon class="wing animated"/>
        </div>
        <div class="wings reversed animated">
          <WingAbstractIcon class="wing reversed animated"/>
          <WingAbstractIcon class="wing reversed animated"/>
        </div>
      </div>
</template>

<style scoped>
@keyframes twist {
 to {
    transform: translateX(0%) rotate(0deg);
 }   
}
.wings-container {
    max-width: 100%;
    display: flex;
    justify-content: space-between;
}
.wings {
    transform: translateX(100%) rotate(-45deg);
    transform-origin: top right;
    animation-name: twist;
}
.wings.reversed {
    transform: translateX(-100%) rotate(45deg);
    transform-origin: top left;
}

@keyframes twistin {
 to {
    transform: scale(1) rotate(0deg);
 }   
}
.wing {
    transform: scale(.5) rotate(-90deg);
    animation-name: twistin;
}

@keyframes reversedtwistin {
 to {
    transform: scale(-1, 1) rotate(0deg);
 }   
}
.wing.reversed  {
    animation-name: reversedtwistin;
    transform: scale(-.5, .5)rotate(-90deg);
}
</style>