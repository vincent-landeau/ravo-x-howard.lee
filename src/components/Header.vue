<script setup>
import {HomeIcon, StoryIcon, PaypalIcon, AppleIcon} from './icons/Icons.js'
import {RavoTextIcon} from './icons/TextIcons.js'
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
      <RavoTextIcon class="animated"/>
      <div class="menu-icon">
        <button>
          <PaypalIcon/>
        </button>
        <button>
          <AppleIcon/>
        </button>
    </div>
  </header>
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
@keyframes zoomin {
  to {
    transform: scale(3);
  }
}
.ravo {
    transform: scale(1);
    animation-name: zoomin;

}
</style>