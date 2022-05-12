<template>
  <div class="gifs-wall">
    <div class="row">
      <div class="column">
        <div v-for="(gif, index) in gifs" :key="index" class="gif">
          <img :src="gif.sorce" :alt="gif.alt" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "GifsWall",
  props: {
    gifs: Array,
  },
};
</script>

<style scoped lang="scss">
.gifs-wall {
  .row {
    display: flex;
    flex-wrap: wrap;
    padding: 0 4px;
  }

  /* Create four equal columns that sits next to each other */
  .column {
    flex: 25%;
    max-width: 25%;
    padding: 0 4px;
  }

  .column .gif {
    margin-top: 8px;
    vertical-align: middle;
    width: 100%;
  }

  /* Responsive layout - makes a two column-layout instead of four columns */
  @media screen and (max-width: 800px) {
    .column {
      -ms-flex: 50%;
      flex: 50%;
      max-width: 50%;
    }
  }

  /* Responsive layout - makes the two columns stack on top of each other instead of next to each other */
  @media screen and (max-width: 600px) {
    .column {
      -ms-flex: 100%;
      flex: 100%;
      max-width: 100%;
    }
  }
  .gif {
    background-color: #42b983;
    width: 100%;
  }
}
</style>
