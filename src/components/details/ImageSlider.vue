<script setup lang="ts">
import { Carousel, Pagination, Slide } from 'vue3-carousel'
import 'vue3-carousel/dist/carousel.css'

const props = defineProps(['images'])
</script>

<template>
  <Carousel>
    <Slide v-for="slide in props.images" :key="slide">
      <div class="carousel__item">
        <img :src="`https://yeahbike.jurczak.dev/img/${slide}.jpg`" class="slide-image" />
      </div>
    </Slide>

    <template #addons>
      <Pagination />
    </template>
  </Carousel>
</template>

<style scoped lang="scss">
.carousel__pagination {
  position: absolute;
  bottom: 12px;
  left: 50%;
  transform: translateX(-50%);
}

:deep(.carousel__pagination-button::after) {
  background-color: #ececeb;
  opacity: 40%;
  width: 8px;
  height: 8px;
  border-radius: 50%;
  transition:
    width 0.2s ease-in-out,
    border-radius 0.2s ease-in-out;
}

:deep(.carousel__pagination-button--active::after) {
  background-color: #ececeb;
  opacity: 100%;
  width: 28px;
  height: 9px;
  border-radius: 8px;
}

.slide-image {
  min-height: 430px;
  object-fit: cover;
}
</style>
