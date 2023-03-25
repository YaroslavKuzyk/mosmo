<template>
  <div>
    <Sales />
    <Header />
    <slot />
  </div>
</template>
<script lang="ts">
import Header from "@/components/layouts/Header.vue";
import Sales from "@/components/layouts/Sales.vue";

export default {
  components: { Header, Sales },
};
</script>
