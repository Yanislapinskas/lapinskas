<template>
  <div>
    <h3 class="q-ma-xs">Бесплатная доставка</h3>
    <div class="row q-ma-xs">
      > 

	<q-carousel
      v-model="slide"
      transition-prev="slide-right"
      transition-next="slide-left"
      animated
      control-color="primary"
      class="rounded-borders"
    >
    <q-carousel-slide name="style" class="column no-wrap flex-center">
        <q-icon name="style" color="primary" size="56px" />
        <div class="q-mt-md text-center">
          {{ lorem }}
        </div>
    </q-carousel-slide>
      <q-carousel-slide name="tv" class="column no-wrap flex-center">
        <q-icon name="live_tv" color="primary" size="56px" />
        <div class="q-mt-md text-center">
          {{ lorem }}
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="layers" class="column no-wrap flex-center">
        <q-icon name="layers" color="primary" size="56px" />
        <div class="q-mt-md text-center">
          {{ lorem }}
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="map" class="column no-wrap flex-center">
        <q-icon name="terrain" color="primary" size="56px" />
        <div class="q-mt-md text-center">
          {{ lorem }}
        </div>
      </q-carousel-slide>
    </q-carousel>

const slide = ref(0 );
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const images = ref([
  "https://avatars.mds.yandex.net/get-eda/2353725/2dc822395bf1d344702e8626e1f7a44f/400x400nocrop",
  "https://avatars.mds.yandex.net/get-feeds-media/5396768/847c53e4539489421bfdfe803b4385ac78dbbddb/orig",
  // Можно добавить другие уникальные изображения
]);

const lorem = ref("test");x
</script>
