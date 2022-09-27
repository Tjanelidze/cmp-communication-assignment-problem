<template>
  <section>
    <form @submit.prevent="submitData">
      <div>
        <label>Name</label>
        <input type="text" v-model="inputName" />
      </div>
      <div>
        <label>Age</label>
        <input type="text" v-model="inputAge" />
      </div>
      <button>Submit</button>
    </form>
  </section>
</template>

<script>
export default {
  emits: ['add-user'],
  data() {
    return {
      inputName: '',
      inputAge: '',
    };
  },
  methods: {
    submitData() {
      this.$emit('add-user', this.inputName, this.inputAge);
      this.inputName = '';
      this.inputAge = '';
    },
  },
};
</script>
