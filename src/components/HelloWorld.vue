<script setup>
import { ref, onMounted } from "vue";
import { VueTelInput } from "vue3-tel-input";
import "vue3-tel-input/dist/vue3-tel-input.css";

const phone = ref(null);

// Define an `onInput` function to handle phone input changes
const onInput = (phone, phoneObject, input) => {
  // console.log("Phone Object:", phoneObject.formatted);
  console.log(phone);
};

onMounted(() => {
  // Set an initial value for the `phone` ref if needed
  phone.value = ""; // Replace with your initial phone number
});
</script>

<template>
  <VueTelInput :value="phone" @input="onInput" mode="international"> </VueTelInput>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
