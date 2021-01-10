<template>
    <div class="card-container">
        <div class="project-card">
           <h3 class="project-title">Lorem Ipsum</h3> 
           <p class="project-description">
               Ipsum project in lamah indiguos it do not matter,
               money got longer, cars got faster turned to a savage.
           </p>
            <a href="" class="project-url">Visit project</a>
        </div>
    </div>
</template>

<script>
import { ref } from 'vue'

export default {
    name: "ProjectCard",
    setup () {
        let fetchedProjects = ref()

        return {
            fetchedProjects
        }

        // TODO: Add section for programming language inside of card..
    }   
}
</script>

<style scoped>
   .project-card {
       @apply border-solid border-4 rounded-lg w-72 shadow-lg;
   } 

   .project-title {
       @apply flex justify-center my-2 font-sans font-bold;
   }

   .project-description {
       @apply flex justify-center px-4;
   }

   .project-url {
       @apply flex justify-center my-4 text-purple-500;
   }
</style>