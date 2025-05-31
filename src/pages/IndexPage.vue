<template>
  <div>
    <h3 class="q-ma-xs">Бесплатная доставка</h3>
    <div class="row q-ma-xs">
      <q-carousel
        v-model="slide"
        transition-prev="slide-right"
        transition-next="slide-left"
        animated
        arrows
        navigation
        control-color="primary"
        class="rounded-borders full-width"
        height="300px"
      >
        <q-carousel-slide
          v-for="(img, index) in images"
          :key="index"
          :name="index"
          class="column no-wrap flex-center bg-grey-2"
        >
          <q-img
            :src="img"
            :alt="'Slide ' + index"
            style="max-height: 100%; max-width: 100%;"
            spinner-color="primary"
          />
        </q-carousel-slide>
      </q-carousel>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const images = ref([
  "https://placekitten.com/600/300",
  "https://placekitten.com/601/300",
  "https://placekitten.com/602/300",
]);

const slide = ref(0);
</script>