<template>
  <section>
    <h2>{{ username }}</h2>
    <h3>{{ age }}</h3>
  </section>
</template>

<script>
export default {
  props: {
    username: {
      type: String,
      required: true,
    },
    age: {
      type: Number,
      required: true,
    },
  },
};
</script>
