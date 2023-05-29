<template>
  <div id="app">
    <AlertDialog :active.sync="show" title="Test Alert" content="Hello world"/>
    <AlertDialog :active.sync="show2" title="Test Alert 2222" content="Hello world 222" confirmText="Yes"/>

    <PopupRemoveVue :active.sync="showPopTest"/>

    <button type="button" @click="show = !show">Alert</button>
    
    <button type="button" @click="show2 = !show2">Alert222</button>

    <button type="button" @click="showPopTest = !showPopTest">Alert222</button>

  </div>
</template>

<script>
import AlertDialog from "./components/AlertDialog.vue";
import PopupRemoveVue from './components/Popup/PopupRemove.vue';

export default {
  name: "app",
  components: {
    AlertDialog,
    PopupRemoveVue
  },
  data() {
    return {
      show: false,
      show2: false,
      showPopTest: false
    };
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
