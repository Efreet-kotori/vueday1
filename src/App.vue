<template>
  <div>
    <!-- 1. 绑定键盘按下事件.enter - 回车 
         2. .esc修饰符 - 取消键-->
    <input type="text" @keydown.enter="enterFn">
    <hr>
    <input type="text" @keydown.esc="escFn">
  </div>
</template>

<script>

export default {
  data() { // 格式固定, 定义vue数据之处
    return {  // key相当于变量名
     
    }
  },
  methods: { // vue 的方法写在 里边
        enterFn(){
     console.log("enter回车按键了");
   },
   escFn(){
     console.log("esc按键了");
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
