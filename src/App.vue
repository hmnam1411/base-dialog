<template>
  <div id="app">
    <BaseDialog :active.sync="show">
      <h1>Test</h1>
      <button type="button" @click="show = !show">Close</button>
    </BaseDialog>
    <button type="button" @click="show = !show">Toggle</button>
  </div>
</template>

<script>
import BaseDialog from "./components/BaseDialog.vue";

export default {
  name: "app",
  components: {
    BaseDialog
  },
  data() {
    return {
      show: false
    };
  }
};
</script>
