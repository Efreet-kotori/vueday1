<template>
  <div id="app">
 <p>你要购买商品的数量: {{ count }}</p>
  <!-- 1. 绑定事件
  语法: v-on:事件名="少量代码"
  语法: v-on:事件名="methods里函数名"
  语法: v-on:事件名="methods里函数名(值)"
  语法: @事件名="methods里函数名"
  -->
  <button v-on:click="count = count + 1">+1</button>
  <button v-on:click="addFn">+1</button>
  <button v-on:click="addCountFn(5)">+5</button>
  <button @click="subFn">减少1</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() { // 格式固定, 定义vue数据之处
    return {  // key相当于变量名
     count:0
    }
  },
  methods: { // vue 的方法写在 里边
            addFn(){ // this代表export default后面的组件对象(下属有data里return出来的属性)
                this.count++
                // this 要注意一下
            },
            addCountFn(num){
                this.count += num
            },
            subFn(){
                this.count--
            }
        }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
