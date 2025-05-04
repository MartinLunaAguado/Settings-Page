<template>
    <Transition mode="out-in" name="fade">
       <slot />
    </Transition>

</template>



<style >
 /* we will explain what these classes do next! */
 .fade-enter-active,
 .fade-leave-active {
   transition: all 0.2s ease;
 }
 
 .fade-enter-from,
 .fade-leave-to {
   opacity: 0;
   scale: 0.95;
 }
 </style>