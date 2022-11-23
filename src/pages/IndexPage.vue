<template>
  <q-page class="">
    <InputComponent @onSubmit="addData" />
    <TableComponent title="Table Data" :columns="columns" :rows="data" />
  </q-page>
</template>

<script>
import { defineComponent, ref } from "vue";
import InputComponent from "src/components/InputComponent.vue";
import TableComponent from "src/components/TableComponent.vue";

export default defineComponent({
  name: "IndexPage",
  components: {
    InputComponent,
    TableComponent,
  },
  setup() {
    const columns = [
      { name: "data", label: "Data", field: (row) => row, align: "left" },
    ];
    const data = ref([]);
    const addData = (val) => {
      data.value.unshift(val);
    };
    return {
      columns,
      data,
      addData,
    };
  },
});
</script>
