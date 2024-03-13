<script setup>
import {MainAbstractIcon, StripesAbstractIcon, InventoryAbstractIcon, ArrowAbstractIcon} from './icons/AbstractIcons.js'
</script>
<template>
    <MainAbstractIcon class="main-abstract animated"/>
    <div class="inventory animated">
      <InventoryAbstractIcon/>
      <span>Inventory</span>
    </div>
    <menu class="animated">
      <li>Home</li>
      <li>Guide Book</li>
      <li>Settings</li>
    </menu>
    <div class="striped-block">
      <StripesAbstractIcon class="animated"/>
    </div>
    <button class="discover animated">
      <span>Discover</span>
      <ArrowAbstractIcon/>
    </button>
</template>

<style scoped>
@keyframes slidein {
  to {
    transform: scale(.9) translate(-50%, -50%);
  }
}
.main-abstract {
  position: absolute;
  top: 36%;
  left: 50%;
    transform: scale(.5) translate(-50%, -50%);
    transform-origin: bottom left;
  animation-name: slidein;
}

@keyframes fadeinx {
 to {
    opacity: 1;
    left: 47px;
 }   
}
.inventory {
    position: absolute;
    top: 20%;
    left: 20px;
    display: flex;
    gap: 0 18px;
    place-items: center;
    opacity: 0;
    animation-name: fadeinx;
}

@keyframes fadeinmenu {
 to {
    opacity: 1;
    transform: translateX(-50%);
 }   
}
menu {
    position: absolute;
    bottom: 47px;
    left: 50%;
    transform: translateX(-300px);
    display: flex;
    justify-content: space-between;
    width: 300px;
    padding: 0;
    opacity: 0;
    animation-delay: .3s;
    animation-name: fadeinmenu;
}

@keyframes fadeiny {
 to {
    opacity: 1;
    transform: translateY(0px);
 }   
}
.striped-block {
    position: absolute;
    bottom: 37px;
    left: 92px;
}
.striped-block svg {
    transform: translateY(47px);
    opacity: 0;
    animation-name: fadeiny;
}
@keyframes stretchin {
 to {
    width: 280px;
    transform: translate(-50%, -50%);
 }   
}
.discover {
  position: absolute;
  left: 50%;
  top: 70%;
  transform: translate(-50%, 100%);
  display: flex;
  place-items: center;
  justify-content: space-between;
  padding: 0 41px;
  font-size: 28px;
  font-weight: 600;
  font-family: "Outfit";
  width: 200px;
  height: 82px;
  border-radius: 41px;
  background-color: rgba(187, 255, 26, 1);
  box-shadow: 0px 4px 50px 0px rgba(187, 255, 26, 1);
  animation-name: stretchin;
}
</style>