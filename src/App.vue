<template>
  <div>
{{fn(arr)}}
  </div>
</template>

<script>

export default {
  data() {
    return {  
       arr : [{a:100}, {a: 20}, {a:-10}]
    };
  },
  methods: {
   fn(arr){
const sum = arr.reduce((pre,curr) => {
  return pre+curr.a
},0)
console.log(sum) // 110
   }
}}
</script>

<style scoped>


</style>