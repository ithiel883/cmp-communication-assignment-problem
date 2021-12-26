<template>
  <div class="grid grid-cols-2 p-4">
    <h2>Username: {{ username }}</h2>

    <h3>Age: {{ age }}</h3>
  </div>
</template>


<script>
export default {
  props: {
    id: {
      type: String,
      required: true,
    },
    username: {
      type: String,
      required: true,
    },
    age: {
      type: String,
      required: true,
    },
  },
};
</script>


<style>

</style>
