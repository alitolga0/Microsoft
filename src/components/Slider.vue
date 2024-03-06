<template>
  <div>
    <transition-group name="fade" tag="div">
      <div v-for="(image, index) in filteredImages" :key="index">
        <img :src="image" />
      </div>
    </transition-group>
    <button @click="toggleSlide">
      <i class="fas fa-play-circle" aria-hidden="true"></i>
    </button>

    <a class="fa fa-chevron-left" @click="prev" href="#"></a>

    <span
      v-for="(image, index) in images"
      :key="index"
      @click="currentIndex = index"
      :class="{ active: currentIndex === index }"
      class="dot"
    ></span>

    <a class="fa fa-angle-right" @click="next" href="#" style="margin-left: 5px;"></a>
  </div>
</template>

<script>
export default {
  name: "mySlider",
  data() {
    return {
      images: [
        require("@/assets/slider1.jpg"),
        require("@/assets/slider2.jpg"),
      ],
      timer: null,
      currentIndex: 0,
    };
  },

  mounted() {
    this.startSlide();
  },

  methods: {
    startSlide() {
      this.timer = setInterval(this.next, 4000);
    },

    next() {
      this.currentIndex = (this.currentIndex + 1) % this.images.length;
    },

    prev() {
      this.currentIndex =
        (this.currentIndex - 1 + this.images.length) % this.images.length;
    },

    toggleSlide() {
      if (this.timer) {
        clearInterval(this.timer);
        this.timer = null;
      } else {
        this.startSlide();
      }
    },
  },

  computed: {
    filteredImages() {
      return [this.images[this.currentIndex]];
    },
  },
};
</script>

<style scoped src="../styles/slider.css"></style>
