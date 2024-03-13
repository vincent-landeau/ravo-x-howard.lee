<script setup>
import {MainTitleTextIcon, DVSTRIAITextIcon} from './icons/TextIcons.js'
import {LineAbstractIcon} from './icons/AbstractIcons.js'
import Wings from './Wings.vue'
</script>
<template>
    <div class="bg">
      <Wings/>
      <MainTitleTextIcon class="main-title animated"/>
    </div>
    <LineAbstractIcon class="line animated"/>
    <DVSTRIAITextIcon class="dvstriai animated"/>
</template>

<style scoped>

.bg {
  position: absolute;
  left: 50%;
  top: 60%;
  transform: translate(-50%, -50%);
}

@keyframes fadein {
 to {
    opacity: 1;
    left: 47px;
 }   
}
.dvstriai {
    position: absolute;
    top: 55%;
    left: 40px;
    transform: translateY(-50%);
    opacity: 0;
    animation-name: fadein;
}

@keyframes stretchin {
  to {
    transform: scaleY(1);
  }
}
.line {
  position: absolute;
  right: 47px;
  bottom: 42px;
    transform: scaleY(0.35);
    transform-origin: 0 0;
    animation-name: stretchin;
}

@keyframes blurin {
  to {
    filter: blur(0);
    transform: scale(1) translateY(0%);
  }
}
.main-title {
    filter: blur(5px);
    transform: scale(1.6) translateY(-50%);
    transform-origin: 50% 0%;
    animation-name: blurin;
}
</style>