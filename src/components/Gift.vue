<template>
  <div class="gift" v-if="gift== true">贈品</div>
</template>

<script>
export default {
    props:['gift']
    
}
</script>

<style>
.gift{
  width:max-content;
  font-size:12px;
  color:#E16D91;
  padding:.5em;
  border: 1px solid #E16D91;
  border-radius: 3px;
  margin:.5rem;
}


</style>