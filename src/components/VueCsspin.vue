<template>
  <div class="modal">
    <div class="box">
        <div class="cp-spinner" :class="spinStyle"></div>
        <div style="margin:1rem;">{{message}}</div>
    </div>
  </div>
</template>

<script>
import 'csspin/csspin.css'

export default {
    name : "VueCsspin",  
    props : {
        message : { type:String, default:"Loading" },
        spinStyle : { type:String, default:"cp-round" },
    } 
}
</script>

<style scoped>
.modal { display: block; position: fixed; z-index: 1; 
    left: 0; top: 0; width: 100%; height: 100%;
    overflow: auto; background-color: rgb(0,0,0); 
    background-color: rgba(0,0,0,0.1); }
.box {   display: flex; flex-direction: column;
    align-items: center; justify-content: center;
    width:100px; height:100px; margin-top: -50px; margin-left:-50px; 
    position: absolute; left: 50%; top: 50%; }
</style>