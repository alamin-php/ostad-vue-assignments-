<script setup>
import { ref } from 'vue';

const images = ref([
  'https://tecdn.b-cdn.net/img/Photos/Slides/img%20(15).jpg',
  'https://tecdn.b-cdn.net/img/Photos/Slides/img%20(16).jpg',
  'https://tecdn.b-cdn.net/img/Photos/Slides/img%20(17).jpg',
  'https://tecdn.b-cdn.net/img/Photos/Slides/img%20(18).jpg',
]);
const currentIndex = ref(0);

const nextSlide = () => {
    if (currentIndex.value < images.value.length - 1) {
        currentIndex.value++;
    }
};

const prevSlide = () => {
    if (currentIndex.value > 0) {
        currentIndex.value--;
    }
};
</script>

<template>
    <div class="carousel-container">
        <div class="carousel">
            <div class="image-wrapper" :style="{ transform: `translateX(-${currentIndex * 100}%)` }">
                <div v-for="(image, index) in images" :key="index" class="image-slide">
                    <img :src="image" alt="Image Slide" />
                </div>
            </div>
        </div>

        <div class="carousel-controls">
            <button @click="prevSlide" :disabled="currentIndex === 0"><i class="fas fa-arrow-left"></i></button>
            <button @click="nextSlide" :disabled="currentIndex === images.length - 1"><i class="fas fa-arrow-right"></i></button>
        </div>
    </div>
</template>

<style scoped>
.carousel-container {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.carousel {
    overflow: hidden;
    width: 100%;
    position: relative;
}

.image-wrapper {
    display: flex;
    transition: transform 0.3s ease-in-out;
}

.image-slide {
    flex: 0 0 100%;
}

img {
    width: 100%;
    height: auto;
}

.carousel-controls {
    margin-top: 10px;
}

button {
    margin: 0 5px;
}
</style>