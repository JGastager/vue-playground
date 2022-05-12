<template>
  <div class="gifs">
    <h1>Random Gif Collection</h1>
    <GifsWall :gifs="gifs" />
  </div>
</template>

<script>
import GifsWall from "@/components/GifsWall.vue";

export default {
  name: "GifsView",
  components: {
    GifsWall,
  },
  data: function () {
    return {
      gifs: [],
    };
  },
  mounted() {
    const fs = require("fs");
    const files = fs.readdirSync("/assets/images/gifs/");
    console.log(files);
  },
};
</script>
