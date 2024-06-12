<template>
    <div class="banner1">
      <div class="banner-content">
        <div class="text">
          <h1>BOOO <img src="@/assets/head1-img.png" alt="ghost emoji"></h1>
          <h1>TRICK OR TREAT!!</h1>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat fugiat velit architecto soluta quos repellendus ipsam expedita doloribus eum iste?</p>
        </div>
        <div class="img">
          <img :src="currentImage" alt="Banner Image">
          <div class="dots">
            <div
              v-for="(dot, index) in images"
              :key="index"
              :class="['dot', { active: activeDot === index + 1 }]"
              @click="toggleImage(index + 1)"
            ></div>
          </div>
        </div>
      </div>
      <div class="scroll" @click="scrollDown">
        <div class="mouse">
          <div class="scroll-wheel"></div>
        </div>
        <p>Scroll</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Section1',
    data() {
      return {
        activeDot: 1,
        images: [
          require('@/assets/Home-banner/home-img1.png'),
          require('@/assets/Home-banner/home-img2.png'),
          require('@/assets/Home-banner/home-img1.png'),
          require('@/assets/Home-banner/home-img2.png'),
          require('@/assets/Home-banner/home-img1.png')
        ]
      };
    },
    computed: {
      currentImage() {
        return this.images[this.activeDot - 1];
      }
    },
    methods: {
      scrollDown() {
        window.scrollBy({
          top: 650,
          behavior: 'smooth'
        });
      },
      toggleImage(dotIndex) {
        this.activeDot = dotIndex;
      }
    }
  };
  </script>
  
