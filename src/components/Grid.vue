<template>
  <div class="flex justify-center">
    <input v-model="currText" class="text-center my-4 flex justify-center" />
    <!-- two way binding to one variable. read and write as you please  -->

    <div id="code-text">
      <code class="text-sm uppercase my-4 font-bold text-red-900 sm:text-gray-900">{{ currText }}</code> 
      <!-- Responsive design; default color is red, gray when screen is larger lhan mobile... -->
    </div>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const currText = ref("");

    return {
      // Anything returned is exposed to the template
      currText
    };
  }
};
</script>

<style>
.my-item {
  border: solid blue 2px;
  border-radius: 4px;
  width: 300px;
  margin: 25px 0px;
}

input {
  border: solid blue 1px;
  border-radius: 3px;
}

#code-text {
  margin: 13px;
}
</style>
