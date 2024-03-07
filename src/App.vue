<template>
  <h1>
    Has published books: {{ hasPublisBook }}
  </h1>
  <hr>
  <h1>
    Has published books: {{ hasPublisBookV2() }}
  </h1>
</template>
<script setup lang="ts">
import {ref , computed} from "vue";
const title = ref({
  name: "Jonh Doe",
  books: [
    "Vue 2 - Advanced Guide ",
    "Vue 3 - Basic Guide",
    "Vue 4 - The Mystery",
  ],
});
const hasPublisBook = computed(() =>{
  return title.value.books.length > 0 ? "YES" : "NO"
})
const hasPublisBookV2 = () => {
  return title.value.books.length > 0 ? "YES" : "NO"
}
</script>
