<template>
  <div id="app">
    <HelloWorld :msg="msg" :msgObj="msgObj"></HelloWorld>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import HelloWorld from './components/HelloWorld.vue';

type DataType = {
  msg: string;
  msgObj: { name: string; age: number; gender: 'man' | 'woman' };
};

export default Vue.extend({
  name: 'App',
  components: {
    HelloWorld,
  },
  data(): DataType {
    return {
      msg: 'Kubota',
      msgObj: { name: 'kubota', age: 44, gender: 'man' },
    };
  },
  methods: {},
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
