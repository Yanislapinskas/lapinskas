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
  "https://avatars.mds.yandex.net/get-eda/2353725/2dc822395bf1d344702e8626e1f7a44f/400x400nocrop",
  "https://avatars.mds.yandex.net/get-feeds-media/5396768/847c53e4539489421bfdfe803b4385ac78dbbddb/orig",
  "https://placekitten.com/400/300",
]);

const slide = ref(0);
</script>