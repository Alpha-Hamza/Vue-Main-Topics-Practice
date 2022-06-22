
<script setup>
import { isRef, reactive, ref,unref, toRefs } from 'vue'
let count = ref(1);

function double() {
    count.value = unref(count) * 2;
    const check = isRef(count) ? count.value : count ;
    console.log(check);

}

const cube = reactive({
length:10,
height:20,
width:30
});
 

const {length,height,width} = toRefs(cube);

</script>
<script >




export default {
    name:"Reactivity",
  
}


</script>

<template>

<h1 class="heading">Reactivity:</h1>
<div class="heading2">
    <h1 >=>refs,unrefs,isRefs:</h1>
    <div class="counter">

        <h2>Counter: {{count}}</h2>
        <button @click="double">press me</button>
    </div>
</div>
<div class="heading3">
    <h1>=>reactivity</h1>
    <div class="data">

        <h1>Length:{{length}}</h1>
        <h1>Height:{{height}}</h1>
        <h1>Width:{{width}}</h1>
    </div>
    
</div>

</template>

<style scoped>
.heading {
 text-align: center;
 margin-top: 50px;
   
}
.counter{
 text-align: center;
}
.counter >button {
   width: 100px;
   height: 50px;
     background: #41b883;
  color: #fff;
  border: 1px #41b883 solid;
  cursor: pointer;
  font-size: 20px;
}
.data {
  margin-left: auto;
  margin-right: auto;
     text-align: center;
        background: #41b883;
  color: #fff;
  border: 1px #41b883 solid;

  font-size: 20px;
  width: 50%;
       
}
.heading2 >h1 {
    color: rebeccapurple;
    margin-top: 30px;
     margin-bottom: 30px;
    font-size: 30px;
}
.heading3 >h1 {
   color: rebeccapurple;
    font-size: 30px;
}

</style>