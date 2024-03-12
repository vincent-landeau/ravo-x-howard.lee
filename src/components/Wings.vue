<script setup>
import {WingAbstractIcon} from "./icons/AbstractIcons.js"
</script>

<template>
    <div class="wings-container">
        <div class="wings">
          <WingAbstractIcon/>
          <WingAbstractIcon/>
        </div>
        <div class="wings reversed">
          <WingAbstractIcon class="reversed"/>
          <WingAbstractIcon class="reversed"/>
        </div>
      </div>
</template>

<style scoped>
@keyframes twistin {
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
    animation-duration: 1s;
    animation-name: twistin;
    animation-timing-function: cubic-bezier(.7,0,.3,1);
    animation-fill-mode: forwards;
}
.wings.reversed {
    transform: translateX(-100%) rotate(45deg);
    transform-origin: top left;
}
</style>