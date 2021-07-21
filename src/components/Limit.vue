<template>
  <div class="text">
      <h2 class="name">{{name}}</h2>
      <span class="sale">{{desc}}</span>
  </div>
</template>

<script >
export default {
    props:['name','desc']
}
</script>

<style>
.text{
    text-align: center;
    color:white;
    width:215px;
    height:198px;
    background-color: #E16D91;
    border-bottom-left-radius: 4px;
    border-bottom-right-radius: 4px;
   
}

.name{
    font-size:15px;
    line-height: 1.4rem;
    
}

.name::before{
        content:'';
        display: block;
        height:4.5rem;
    }

.sale{
    font-size:22px;
}
</style>