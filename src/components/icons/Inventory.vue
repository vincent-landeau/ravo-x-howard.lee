<template>
    <div class="inventory">
        <svg width="14" height="47" id="evkeI3ma7Uc1" viewBox="0 0 14 47" shape-rendering="geometricPrecision" text-rendering="geometricPrecision">
            <path d="M0,7.274004l14,14v5l-14-14v-5Z" transform="matrix(1 0 0-1 0 54.274004)" stroke-width="0.5" fill="black"/>
            <path d="M0.10044,37v-5l8.46867-8.46867L0,14.96222v-5L13.56911,23.53133Q1.447307,35.653133,0.10044,37Z" stroke-width="0.5" fill="black"/>
            <path d="M3.56911,23.53133C2.28933,24.81111,1.09963,26.00081,0,27.10044v-7.13822l3.56911,3.56911Z" stroke-width="0.5" fill="black"/>
            <path d="M0,7.274004l14,14v5l-14-14v-5Z" transform="translate(0-7.274004)" stroke-width="0.5" fill="black"/>
        </svg>
      <span>Inventory</span>
    </div>
</template>

<style scoped>
@keyframes fadein {
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
    animation-duration: 1s;
    animation-name: fadein;
    animation-timing-function: cubic-bezier(.7,0,.3,1);
    animation-fill-mode: forwards;
}

</style>