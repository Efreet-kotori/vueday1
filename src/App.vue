<template>
  <div>
{{fn(arr)}}
{{sn(str.split(""))}}
  </div>
</template>

<script>

export default {
  data() {
    return {  
       arr : [{a:100}, {a: 20}, {a:-10}],
       str:'asdasdasdasaaasdsadsa'
    };
  },
  methods: {
   fn(arr){
const sum = arr.reduce((pre,curr) => {
  return pre+curr.a
},0)
console.log(sum) // 110
   },
   sn(names ){
    let countedNames = names.reduce(function (allNames, name) {
  if (name in allNames) {
    allNames[name]++
  }
  else {
    allNames[name] = 1
  }
  return allNames
}, {})
console.log(countedNames);
   }
}}
</script>

<style scoped>


</style>