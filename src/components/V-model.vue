

<template>
<div class="vmodel">

    <h1 class="heading">V-Model and $emit:</h1>
     
    <input  type="text" :value="modelValue" @input="updateValue"  />
</div>
  
</template>

<script >




export default {
   name:"VModel",
   props: {
    modelValue:{
       
            type: String,
           
   
    } 
    
   }
,
 methods: {
        updateValue(event) {
            this.$emit('update:modelValue', event.target.value);
        }
    }
   
}
</script>

<style scoped >
.heading {
  margin-top: 50px;
 text-align: center;
   
}
.vmodel >input {
    color: black;
  border: 1px #41b883 solid;
  height: 30px;
}

</style>
