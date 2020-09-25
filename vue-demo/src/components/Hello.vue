<template>
  <div>
    <h1>hello vue {{name}}</h1>
    <el-radio v-model="radio" label="1">备选项1</el-radio>
    <el-radio v-model="radio" label="2">备选项2</el-radio>
    <button @click='hello'>test $</button>
  </div>
</template>
<script>
export default {
  name: 'mycom',
  data () {
    return {
      name: "张三",
      radio: 1
    };
  },
  methods: {
    hello () {
      this.$myMethods('hello')
    },
    myMethods (msg) {
      alert(msg)
    }
  },
  created () {
    this.$myMethods = this.myMethods
  },
};
</script>
<style>
</style>
