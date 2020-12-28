<template>
   <form>
       <div>
            <label for="name" class="user-input-label"> > Name</label>
            <input type="text" name="name" class="user-input">
       </div>

       <div>
           <label for="email" class="user-input-label"> > Email</label>
           <input type="text" name="email" class="user-input">
       </div>

       <div>
           <label for="subject" class="user-input-label"> > Subject</label>
           <input type="text" name="subject" class="user-input">
       </div>

       <div>
           <label for="message" class="user-input-label"> > Message</label>
           <textarea class="block rounded my-2 px-2 h-48 w-60 border-2 border-blue-300"></textarea>
       </div>

       <div class="flex justify-center">
           <button class="rounded-full py-2 px-6 my-6 uppercase font-bold font-mono cursor-pointer border-blue-300 border-2">
               Send
           </button>
       </div>
   </form>
</template>

<script>
// import axios from 'axios'

export default {
   name: "ContactForm",
   setup() {

   }
}
</script>

<style>
   .user-input {
       @apply block my-2 px-2 rounded border-solid border-2 border-blue-300 w-60;
    } 

    .user-input-label {
       @apply font-mono font-bold; 
    }
</style>