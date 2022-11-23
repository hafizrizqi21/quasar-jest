<template lang="">
  <form @submit.prevent="submit">
    <q-input outlined v-model="input" />
  </form>
</template>
<script>
import { ref } from "vue";

export default {
  setup(_, { emit }) {
    const input = ref("");
    const submit = () => {
      emit("onSubmit", input.value);
      input.value = "";
    };
    return {
      input,
      submit,
    };
  },
};
</script>
<style lang=""></style>
