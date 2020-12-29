<template>
  <NavBar></NavBar>

  <div class="fixed my-4 flex flex-col items-center">
    <img src="@/assets/images/github.svg"   alt="github"   class="svg-icon">
    <img src="@/assets/images/linkedin.svg" alt="linkedin" class="svg-icon">
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

   <div class="flex justify-center">
        <ContactForm/>
   </div>

</template>

<script>

import ContactForm from "@/components/ContactForm.vue";
import NavBar from "@/components/NavBar.vue"

export default {
  name: "Home",
  components: {
    ContactForm, NavBar
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
