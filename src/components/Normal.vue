<template>
  <div class="textN">
    <h2 class="nameN">{{ name }}</h2>
    <span class="priceN">{{ price }}</span>
  </div>
</template>

<script >
export default {
  props: ["name", "price"],
};
</script>

<style>
.textN {
  width: 200px;
  padding: 0.5rem;
}

.nameN {
  font-size: 15px;
  line-height: 1.4rem;
}

.priceN {
  color: #ea3323;
  font-weight: bold;
  display: block;
  margin: 1rem 0;
}
</style>