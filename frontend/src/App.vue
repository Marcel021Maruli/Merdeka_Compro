<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->    
  
     <router-view/>

    
  </div>
</template>
<script>
export default {
  name: 'app'
}
</script>
<style lang="scss">
@import '@/assets/scss/global-variable.scss';

*{

padding:0px;
margin:0px;
font-family: 'poppins',sans-serif;

}

.red-line{
    width:50%;
    height:10px;
    background-color: #CB2B2B;
    border-radius: 9px;
    margin-bottom:50px;

}



</style>
