<template>
   <nav class="bg-gray-800 h-14">
       <div class="flex items-baseline space-x-4 py-4 px-2 text-white font-mono justify-center">
           <a href="" class="nav-items">Home</a>
           <a href="" class="nav-items">Projects</a>
           <a href="" class="nav-items">Contact</a>
       </div>
   </nav>
</template>

<script>
export default {
   name: "NavBar" 
}
</script>

<style>
   .nav-items {
       @apply hover:bg-gray-700 font-medium rounded-md px-3;
   } 
</style>