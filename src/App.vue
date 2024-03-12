<script setup>
import {HomeIcon, StoryIcon, PaypalIcon, AppleIcon} from './components/icons/Icons.js'
import {RavoTextIcon, MainTitleTextIcon, DVSTRIAITextIcon} from './components/icons/TextIcons.js'
import {LineAbstractIcon, MainAbstractIcon, StripesAbstractIcon, InventoryAbstractIcon} from './components/icons/AbstractIcons.js'
import Menu from './components/Menu.vue'
import Character from './components/Character.vue'
import Wings from './components/Wings.vue'
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
      <Wings/>
      <MainTitleTextIcon />
    </div>
    <Character/>
    <MainAbstractIcon/>
    <Menu/>
    <StripesAbstractIcon/>
    <DVSTRIAITextIcon/>
    <InventoryAbstractIcon/>
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

@media (min-width: 1024px) {

}
</style>
