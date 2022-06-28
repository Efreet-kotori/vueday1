<template>
  <div >
{{fn(url)}}
  </div>
</template>

<script>

export default {
  data() {
    return {  
      url:'http://www.baidu.com?name=zhangsan&age=18&sex=nan#'
    };
  },
  methods: {
fn(url){
  const index1 = url.indexOf('?'),
        index2 = url.indexOf('#'),
        params = url.slice(index1+1,index2 ).split('&')
  return params.reduce((pre,curr)=>{
    const [key,value] = curr.split('=')
    pre[key] = value
    return pre
  },{})
}
  }
}
</script>

<style scoped>


</style>