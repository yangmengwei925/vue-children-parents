<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <div class="box">
      我是父组件
      <p>
        {{newStr}}
      </p>
    </div>
    <NewVue @zxcv="acceptMsg" />
  </div>
</template>

<script>
import NewVue from './components/newVue'
export default {
  name: 'app',
  components: {
    NewVue
  },
  data() {
    return {
      num: 999999,
      count: 0,
      test: 10,
      newStr: ''
    }
  },
  methods: {
    addCount() {
      this.count++
    },
    acceptMsg(data) {
      this.newStr = data
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.box{
  width: 100%;
  height: 200px;
  background: skyblue;
}
</style>
