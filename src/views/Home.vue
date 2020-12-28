<template>
  <div class="flex justify-center">
    <!-- On mobile make it full width and on larger devices make it 3 quarters of width -->
    <div class="flex justify-center w-10/12 sm:w-8/12 my-8">
      <ul id="menu">
        <li>Home</li>
        <li>Projects</li>
      </ul>
    </div>
  </div>

   <div class="flex justify-center">
        <ContactForm/>
    </div>
</template>

<script>
// import Grid from "@/components/Grid.vue"

import ContactForm from "@/components/ContactForm.vue";

export default {
  name: "Home",
  components: {
    ContactForm
  },
  setup() {}
};
</script>

<style scoped>
#menu {
  list-style-type: lower-roman;
  margin: 30px 0px;
}

</style>
