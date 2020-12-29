<template>
   <form @submit.prevent>
       <div>
            <label for="name" class="user-input-label"> > Name</label>
            <input v-model="name" type="text" name="name" class="user-input">
       </div>

       <div>
           <label for="email" class="user-input-label"> > Email</label>
           <input v-model="email" type="text" name="email" class="user-input">
       </div>

       <div>
           <label for="subject" class="user-input-label"> > Subject</label>
           <input v-model="subject" type="text" name="subject" class="user-input">
       </div>

       <div>
           <label for="message" class="user-input-label"> > Message</label>
           <textarea v-model="message" class="block rounded my-2 px-2 h-48 w-60 border-2 border-blue-300"></textarea>
       </div>

       <div class="flex justify-center">
           <button 
           
           @click="submitForm"
           class="rounded-full py-2 px-6 my-6 uppercase font-bold font-mono cursor-pointer bg-blue-300 hover:bg-green-300">
               Send
           </button>
       </div>
   </form>
</template>

<script>
// import axios from 'axios'
import { ref } from 'vue'

export default {
   name: "ContactForm",
   setup() {

       let name, subject, email, message = ref("")

       function submitForm() {
           console.log("Make POST request to server.")
       }

       return {
           name,
           subject,
           email,
           message,
           submitForm
       }
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