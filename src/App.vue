<template>
  <div id="app">
    
    <component-vue></component-vue>
  </div>
</template>
<script>
import ComponentVue from "./components/ComponentVue.vue";
export default {
  components: { ComponentVue },
  name: "app",

  data() {
    return {};
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="less">
* {
  padding: 0;
  margin: 0;
}
</style>
