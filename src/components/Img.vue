<template>
  <div class="img_inner mx-auto">
      <img class="img_resp" :src="src" :alt="name" width="400" height="400">
  </div>
</template>

<script>
export default {
   props: ["src", "name"],
}
</script>

<style>
.img_inner{
    width: 200px;
    height: 200px;
   
}

.img_resp{
    width: 100%;
    height:auto;
}
</style>