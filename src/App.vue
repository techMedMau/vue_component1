
<template>
  <div id="app" class="container mx-auto flex">
    <div class="card" v-for="(item, index) in data" :key="index">
      <span v-if="data[index].hasFast == true"
        ><Fast :fast="data[index].hasFast"
      /></span>

      <Img :src="data[index].src" :name="data[index].name" />
      <span v-if="data[index].hasLimit == true"
        ><Limit :name="data[index].name" :desc="data[index].desc"
      /></span>
      <span v-else
        ><Normal :name="data[index].name" :price="data[index].price"
      /></span>
      <span v-if="data[index].hasGift == true"
        ><Gift :gift="data[index].hasGift"
      /></span>
    </div>
  </div>
</template>

<script>
import Img from "@/components/Img";
import Normal from "@/components/Normal";
import Limit from "@/components/Limit";
import Gift from "@/components/Gift";
import Fast from "@/components/Fast";

export default {
  name: "App",
  components: {
    Img,
    Normal,
    Limit,
    Gift,
    Fast,
  },
  data() {
    return {
      data: [],
    };
  },
  created() {
    this.$http.get("../static/data.json").then((res) => {
      this.data = res.data;
    });
  },
};
</script>

<style>
* {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
}

.container {
  max-width: 1200px;
}

.mx-auto {
  margin-right: auto;
  margin-left: auto;
}

.flex {
  display: flex;
  flex-wrap: wrap;
}

.card {
  border: 1px solid #dddddd;
  width: max-content;
  border-radius: 4px;
  margin: 10px;
}
</style>
