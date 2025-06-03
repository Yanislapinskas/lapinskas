<template>
  <div>
    <h3 class="q-ma-xs">Бесплатная доставка</h3>
	   <div class="my-swiper">
		<Swiper
		  :slides-per-view="1"
		  :space-between="20"
		  :navigation="true"
		  :pagination="{ clickable: true }"
		  :breakpoints="{
			640: { slidesPerView: 1 },
			768: { slidesPerView: 2 },
			1024: { slidesPerView: 3 },
			1280: { slidesPerView: 4 }
		  }"
		>
		  <SwiperSlide v-for="slide in slides" :key="slide.id">
			<q-card class="my-slide">
			  <q-img :src="slide.image" :alt="slide.title" />
			  <q-card-section>
				<div class="text-h6">{{ slide.title }}</div>
			  </q-card-section>
			</q-card>
		  </SwiperSlide>
		</Swiper>
	  </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'

import SwiperCore, { Navigation, Pagination } from 'swiper'

SwiperCore.use([Navigation, Pagination])

const slides = ref([
  { id: 1, title: 'Слайд 1', image: 'https://avatars.mds.yandex.net/get-eda/2353725/2dc822395bf1d344702e8626e1f7a44f/400x400nocrop'  },
  { id: 2, title: 'Слайд 2', image: 'https://avatars.mds.yandex.net/get-feeds-media/5396768/847c53e4539489421bfdfe803b4385ac78dbbddb/orig'  },
  { id: 3, title: 'Слайд 3', image: 'https://avatars.mds.yandex.net/get-eda/2353725/2dc822395bf1d344702e8626e1f7a44f/400x400nocrop'  },
  { id: 4, title: 'Слайд 4', image: 'https://avatars.mds.yandex.net/get-feeds-media/5396768/847c53e4539489421bfdfe803b4385ac78dbbddb/orig'  },
]);

</script> 

<style scoped>
.my-swiper {
  width: 100%;
  max-width: 1200px;
  margin: auto;
}

.my-slide {
  height: 300px;
  display: flex;
  flex-direction: column;
}
</style>