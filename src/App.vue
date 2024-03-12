<script setup>
import {HomeIcon, StoryIcon, PaypalIcon, AppleIcon} from './components/icons/Icons.js'
import {RavoTextIcon, MainTitleTextIcon, DVSTRIAITextIcon} from './components/icons/TextIcons.js'
import {LineAbstractIcon, MainAbstractIcon, StripesAbstractIcon, InventoryAbstractIcon, WingAbstractIcon} from './components/icons/AbstractIcons.js'
import CharacterImage from './assets/character.png'
</script>

<template>
  <header>
      <div class="menu-icon">
        <button>
          <HomeIcon/>
        </button>
        <button>
          <StoryIcon/>
        </button>
      </div>
      <RavoTextIcon/>
      <div class="menu-icon">
        <button>
          <PaypalIcon/>
        </button>
        <button>
          <AppleIcon/>
        </button>
    </div>
  </header>

  <main>
    <div class="line">
      <LineAbstractIcon />
    </div>
    <div class="main-title">
      <div class="wings-container">
        <div class="wings">
          <WingAbstractIcon/>
          <WingAbstractIcon/>
        </div>
        <div class="wings reversed">
          <WingAbstractIcon/>
          <WingAbstractIcon/>
        </div>
      </div>
      <MainTitleTextIcon />
    </div>
    <div class="character">
      <img :src=CharacterImage>
    </div>
    <div class="main-abstract">
      <MainAbstractIcon/>
    </div>
    <menu>
      <li>Home</li>
      <li>Guide Book</li>
      <li>Settings</li>
    </menu>
    <div class="striped-block">
      <StripesAbstractIcon/>
    </div>
    <div class="dvstriai">
      <DVSTRIAITextIcon/>
    </div>
    <div class="inventory">
      <InventoryAbstractIcon/>
      <span>Inventory</span>
    </div>
  </main>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  width: 100vw;
  padding: 2rem;
  font-weight: normal;
  line-height: 1.5;
  place-items: center;
}

button {
  border-radius: 50%;
  padding: 12px;
  margin: 4px;
  aspect-ratio: 1/1;
  background-color: rgba(224, 226, 240, 1);
}

.line {
  position: absolute;
  right: 47px;
  bottom: 42px;
}

.main-title {
  position: absolute;
  left: 50%;
  top: 60%;
  transform: translate(-50%, -50%);
}

.main-abstract {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%) scale(.85);
}

.character {
  position: absolute;
  top: 2%;
  left: 55%;
  transform: translateX(-50%);
}

.character > img {
  height: 110vh;
}

menu {
  position: absolute;
  bottom: 7%;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  justify-content: space-between;
  width: 300px;
  padding: 0;
}

.striped-block {
  position: absolute;
  bottom: 47px;
  left: 92px;
}

.dvstriai {
  position: absolute;
  top: 55%;
  left: 47px;
  transform: translateY(-50%);
}

.inventory {
  position: absolute;
  top: 20%;
  left: 47px;
  display: flex;
  gap: 0 18px;
  place-items: center;
}

.wings-container {
  width: 710px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}

.wings.reversed svg {
  transform: scale(-1, 1);
}

@media (min-width: 1024px) {

}
</style>
