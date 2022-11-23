<template lang="">
  <div>
    <q-table :title="title" :rows="rows" :columns="columns" />
  </div>
</template>
<script>
export default {
  props: {
    title: String,
    columns: [],
    rows: [],
  },
  setup(props) {},
};
</script>
<style lang=""></style>
