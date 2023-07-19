<template>
  <el-config-provider namespace="ep">
    <h1>selecteds not active</h1>
    <div style="display: flex; width: 100%; justify-content: space-around">
      <div>
        <h3>selected items</h3>
        <pre>{{ selecteds }}</pre>
      </div>
      <div>
        <h3>options</h3>
        <pre>{{ options }}</pre>
      </div>
    </div>
    <el-select v-model="selecteds" multiple placeholder="Select">
      <el-option
        v-for="item in options"
        :key="item.value"
        :label="item.label"
        :value="item.value"
      />
    </el-select>
  </el-config-provider>
</template>

<script lang="ts" setup>
import { ref } from "vue";

const selecteds = ref([
  {
    value: "Option1",
    label: "Option1",
  },
]);

const options = [
  {
    value: "Option1",
    label: "Option1",
  },
  {
    value: "Option2",
    label: "Option2",
  },
  {
    value: "Option3",
    label: "Option3",
  },
  {
    value: "Option4",
    label: "Option4",
  },
  {
    value: "Option5",
    label: "Option5",
  },
];
</script>
