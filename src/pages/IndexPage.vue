<template>
  <h3 class="q-ma-xs">
	Бесплатная доставка
  </h3>
  <div class="row q-ma-xs">
  
    <q-carousel
      v-model="slide"
      transition-prev="slide-right"
      transition-next="slide-left"
      animated
      control-color="primary"
      class="rounded-borders"
    >
      <q-carousel-slide v-for="(image,index) in images" :key="index" name="style" class="column no-wrap flex-center">
	  
		<q-card  class="col-4" style="height: 200px;">
		  <q-img 
			height="100%"
			:src="image"
		  >
			<div class="absolute-bottom text-h6">
			  Title {{index}}
			</div>
		  </q-img>
		</q-card>
	  </q-carousel-slide>
    </q-carousel>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const images = ref([
"https://avatars.mds.yandex.net/get-eda/2353725/2dc822395bf1d344702e8626e1f7a44f/400x400nocrop",
"https://avatars.mds.yandex.net/get-eda/2353725/2dc822395bf1d344702e8626e1f7a44f/400x400nocrop",
"https://avatars.mds.yandex.net/get-eda/2353725/2dc822395bf1d344702e8626e1f7a44f/400x400nocrop",
"https://avatars.mds.yandex.net/get-feeds-media/5396768/847c53e4539489421bfdfe803b4385ac78dbbddb/orig",
"https://avatars.mds.yandex.net/get-eda/2353725/2dc822395bf1d344702e8626e1f7a44f/400x400nocrop",
"https://avatars.mds.yandex.net/get-eda/2353725/2dc822395bf1d344702e8626e1f7a44f/400x400nocrop",
"https://avatars.mds.yandex.net/get-eda/2353725/2dc822395bf1d344702e8626e1f7a44f/400x400nocrop",
"https://avatars.mds.yandex.net/get-eda/2353725/2dc822395bf1d344702e8626e1f7a44f/400x400nocrop",
"https://avatars.mds.yandex.net/get-eda/2353725/2dc822395bf1d344702e8626e1f7a44f/400x400nocrop",
])
</script>