<script >
let a = 1;
import VBind from './components/V-bind.vue';
import VModel from './components/V-model.vue';
import Watch from './components/watch.vue';
import Reactivity from './components/Reactivity.vue';


export default {
    name: "App",
    components: { VBind, VModel, Watch, Reactivity },

    data() {
    return {

      Name: "jane",
    }

   },
 
}

</script>

<template>

<div class="app">

  <VBind :Name="Name"/>
  <VModel v-model="Name"/>
  <p>{{Name}}</p>
  <Watch />
  <Reactivity />
</div>





</template>
<style >

.app{
background-color: #08BDE5;
  width:500px;
  margin-left: auto;
  margin-right: auto;
}
.app >p{
  color: #2008E5;
  font-size: 30px;
  font-weight: 600;
}


</style>


