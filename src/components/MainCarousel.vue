<template>
  <v-carousel
    v-model="model"
    :cycle="true"
    :show-arrows-on-hover="true"
    height="600"
  >
    <v-carousel-item
      v-for="(item, i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
    >
<!--      <v-sheet-->
<!--        height="100%"-->
<!--        tile-->
<!--      >-->
<!--        <v-row-->
<!--          class="fill-height"-->
<!--          align="center"-->
<!--          justify="center"-->
<!--        >-->
<!--          <div class="display-3">-->
<!--            Slide {{ i + 1 }}-->
<!--          </div>-->
<!--        </v-row>-->
<!--      </v-sheet>-->
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  data: () => ({
    model: 0,
    colors: [
      'primary',
      'secondary',
      'yellow darken-2',
      'red',
      'orange',
    ],
    items: [
      {
        src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
      },
      {
        // eslint-disable-next-line global-require
        src: require('../assets/images/2-nature.jpg'),
      },
      {
        // eslint-disable-next-line global-require
        src: require('../assets/images/River1.jpg'),
      },
    ],
  }),
};
</script>
