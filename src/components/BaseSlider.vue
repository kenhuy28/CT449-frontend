<template>
   <div class="slider-box">
      <div class="slider-content">
         <Splide :options="options" aria-label="My Favorite Images">
            <SplideSlide>
               <img src="http://cdn.shopify.com/s/files/1/0538/7249/2712/collections/Huffkins_Biscuits_1200x1200.jpg?v=1665651984" alt="Sample 2" />
            </SplideSlide>
            <SplideSlide>
               <img src="https://cdn.shopify.com/s/files/1/0631/8804/1949/collections/collection-banner-2_d8208d36-220a-4459-91d6-174e9fb64f0e.jpg?v=1649063431&width=1500" alt="Sample 1" />
            </SplideSlide>

         </Splide>
      </div>
   </div>
</template>

<script>
import { Splide, SplideSlide } from "@splidejs/vue-splide";
import { defineComponent } from "vue";

export default defineComponent({
   components: {
      Splide,
      SplideSlide,
   },

   setup() {
      const options = {
         rewind: true,
         gap: "1rem",
         autoplay: true,
      };

      return { options };
   },
});
</script>

<style scoped>
.splide__slide img {
   width: 100%;
   height: 300px;
   object-fit: cover; /* Bao phủ toàn bộ khung hình */
   display: block;
}
.content {
   margin-top: 5px;
   position: absolute; /* Để đưa nội dung vào trong khung ảnh */
   right: 10px;
   bottom: 20px;
   width: 400px;
   text-align: justify;
   background-color: #333;
   padding: 7px 7px 12px;
   border-radius: 3px;
   opacity: 0.85;
}
.content a {
   text-decoration: none;
   color: white;
   display: inline-block;
   line-height: 24px;
   text-transform: uppercase;
}
</style>
