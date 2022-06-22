

<template>
 <div class="vbind">

    <h1 class="heading">V-bind:</h1>
     
       <h1 class="data" >{{Name}}</h1>
 </div>


  
</template>

<script >




export default {
   name:"VBind",
   props: {
    Name: String,
    
   }
   
}
</script>

<style scoped >


.heading {
 text-align: center;
   
} 
.data {
   text-align: center;
   color: #2008E5;
 
}

</style>
