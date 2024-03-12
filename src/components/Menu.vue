<template>
    <menu>
      <li>Home</li>
      <li>Guide Book</li>
      <li>Settings</li>
    </menu>
</template>

<style scoped>
@keyframes fadein {
 to {
    opacity: 1;
    transform: translateX(-50%);
 }   
}
menu {
    position: absolute;
    bottom: 7%;
    left: 50%;
    transform: translateX(-300px);
    display: flex;
    justify-content: space-between;
    width: 300px;
    padding: 0;
    opacity: 0;
    animation-delay: .2s;
    animation-duration: 1s;
    animation-name: fadein;
    animation-timing-function: cubic-bezier(.7,0,.3,1);
    animation-fill-mode: forwards;
}
</style>