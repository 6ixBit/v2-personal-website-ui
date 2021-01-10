<template>
  <NavBar></NavBar>

  <div class="fixed my-4 flex flex-col items-center">
    <img src="@/assets/images/github.svg"   alt="github"   class="svg-icon" @click="redirectToGit()">
    <img src="@/assets/images/linkedin.svg" alt="linkedin" class="svg-icon" @click="redirectToLinkedin()">
  </div>

  <div class="flex justify-center">
    <!-- On mobile make it full width and on larger devices make it 3 quarters of width -->
    <div class="flex justify-center w-10/12 sm:w-8/12 my-8">
      <ul id="menu">
        <!-- <li>Home</li>
        <li>Projects</li> -->
      </ul>
    </div>
  </div>

  <div>
    <ProjectCard/>
  </div>

   <div class="flex justify-center">
        <ContactForm/>
   </div>

</template>

<script>
import ContactForm from "@/components/ContactForm.vue";
import NavBar from "@/components/NavBar.vue";
import ProjectCard from "@/components/ProjectCard.vue";

export default {
  name: "Home",
  components: {
    ContactForm, NavBar, ProjectCard
  },
  setup() {
    function redirectToGit() {
      window.location = process.env.VUE_APP_GITHUB_URL;
    }

    function redirectToLinkedin() {
      window.location = process.env.VUE_APP_LINKEDIN_URL;
    }

    return {
      redirectToGit,
      redirectToLinkedin
    }
  }
};
</script>

<style scoped>
#menu {
  list-style-type: lower-roman;
  margin: 30px 0px;
}

.svg-icon {
  @apply my-1 mx-1 h-10 cursor-pointer;
}
</style>
