<template>
  <div :class="`grid grid-rows-${rows} grid-cols-${cols} gap-${gap}`">
    <slot></slot>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Grid",
  props: {
    rows: { type: [String, Number], required: true },
    cols: { type: [String, Number], required: true },
    gap: { type: [String, Number], defualt: 0 },
  },
});
</script>
