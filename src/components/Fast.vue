<template>
  <div class="fast" v-if="fast== true">24H</div>
</template>

<script>
export default {
    props:['fast']
}
</script>

<style>
.fast{
  font-size:12px;
  color:#fff;
  padding:.5em;
 background-color: #BB261A;
  border-radius: 3px;
  font-weight: 500;
 width:max-content;
  margin:.5rem;
}

</style>