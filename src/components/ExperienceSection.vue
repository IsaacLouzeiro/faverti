<script>
    // import Swiper core and required modules
    import { Navigation, Pagination, Autoplay, A11y } from 'swiper';

    // Import Swiper Vue.js components
    import { Swiper, SwiperSlide } from 'swiper/vue';

    // Import Swiper styles
    import 'swiper/css';
    import 'swiper/css/navigation';
    import 'swiper/css/pagination';

    // Import Swiper styles
    export default {
        data() {
          return {
            testimonials: [
              {
                name: "Bill Gates",
                testimonial: "Devemos aproveitar o poder da tecnologia da informação para impulsionar a sustentabilidade, pois o futuro não pode ser digital sem também ser verde.",
                business: "Magnata"
              },
              {
                name: "Angelo Fígaro",
                testimonial: "Por meio das novas tecnologias, a gente precisa ajudar o colaborador a ser mais humano e menos mecânico.",
                business: "CIO LATAM Renault"
              },
              {
                name: "Gro Harlem Brundtland",
                testimonial: "Sustentabilidade é suprir as necessidades da geração presente, sem afetar a habilidade das gerações futuras de suprir as suas.",
                business: "Diplomata"
              },
              {
                name: "Jeffrey Sachs",
                testimonial: "Desenvolvimento sustentável significa prosperidade globalmente compartilhada e ambientalmente sustentável.",
                business: "Economista"
              }
            ]
          }
        },
        components: {
        Swiper,
        SwiperSlide,
        },
        
        setup() {
            const onSwiper = (swiper) => {
                console.log(swiper);
            };
            const onSlideChange = () => {
                console.log('slide change');
            };
            return {
                onSwiper,
                onSlideChange,
                modules: [Navigation, Pagination, Autoplay, A11y]
            };
        },
    };
</script>

<template>
    <!-- ======= Testimonials Section ======= -->
    <section id="testimonials" class="testimonials section-bg">
        <div class="container">
            <div class="section-title">
                <span>Depoimentos</span>
                <h2>Depoimentos</h2>
                <p>Seja o primeiro a aparecer aqui, mande nos uma hístória &#128516;</p>
            </div>
            
            <swiper
                :modules="modules"
                :speed= 600
                :loop= false
                :autoplay="{ delay: 5000, disableOnInteraction: false }"
                :breakpoints="{320: { slidesPerView: 1, spaceBetween: 20 }, 1200: { slidesPerView: 3, spaceBetween: 20}}"
            
                :navigation="{ el: '.swiper-pagination', type: 'bullets',clickable: true, nextEl: 'null', prevEl: 'null' }"
                :pagination="{ clickable: true }"
                @swiper="onSwiper"
                @slideChange="onSlideChange"
            >
                <swiper-slide 
                  v-for="testimonial in testimonials"
                  :key="testimonial"
                >
                    <div class="testimonial-item">
                        <p>
                          <i class="bi bi-quote"></i>
                          {{ testimonial.testimonial }}
                          <i class="bi bi-quote" style="transform: rotate(180deg); display: inline-block;"></i>
                        </p>
                        <h3>{{ testimonial.name }}</h3>
                        <h4>{{ testimonial.business }}</h4>
                    </div>
                </swiper-slide><!-- End testimonial item -->
            </swiper>
        </div>
    </section><!-- End Testimonials Section -->

    <!-- ======= Cta Section ======= -->
    <section id="cta" class="cta">
      <div class="container">
        <div class="text-center">
          <h3>Conte sua experiência</h3>
          <p>Mande uma história para nós através do Email, contando sobre uma experiência sua relacionada a TI Verde &#128516;. A história mais interessante será colocada no site &#128151;.</p>
          <a class="cta-btn" href="mailto:faverti@gmail.com">Conte sua experiência</a>
        </div>
      </div>
    </section><!-- End Cta Section -->
</template>

<style scoped>
/*--------------------------------------------------------------
# Testimonials
--------------------------------------------------------------*/
.testimonials .testimonials-carousel,
.testimonials .testimonials-slider {
  overflow: hidden;
}

.testimonials .testimonial-item {
  box-sizing: content-box;
  min-height: 320px;
}

.testimonials .testimonial-item .bi {
    color: #e4e6ea;
    font-size: 26px;
}

.testimonials .testimonial-item h3 {
  font-size: 18px;
  font-weight: bold;
  margin: 10px 0 5px 45px;
  color: #111;
}

.testimonials .testimonial-item h4 {
  font-size: 14px;
  color: #999;
  margin: 0 0 0 45px;
}

.testimonials .testimonial-item .quote-icon-left,
.testimonials .testimonial-item .quote-icon-right {
  color: #e4e6ea;
  font-size: 26px;
}

.testimonials .testimonial-item .quote-icon-left {
  display: inline-block;
  left: -5px;
  position: relative;
}

.testimonials .testimonial-item .quote-icon-right {
  display: inline-block;
  right: -5px;
  position: relative;
  top: 10px;
}

.testimonials .testimonial-item p {
  font-style: italic;
  margin: 0 15px 0 15px;
  padding: 20px 20px 60px 20px;
  background: white;
  position: relative;
  border-radius: 6px;
  position: relative;
  z-index: 1;
}

.testimonials .swiper-pagination {
  margin-top: 20px;
  position: relative;
}

.testimonials .swiper-pagination .swiper-pagination-bullet {
  width: 12px;
  height: 12px;
  background-color: #fff;
  opacity: 1;
  border: 1px solid #16df7e;
}

.testimonials .swiper-pagination .swiper-pagination-bullet-active {
  background-color: #16df7e;
}

/*--------------------------------------------------------------
# Cta
--------------------------------------------------------------*/
.cta {
  background: #16df7e;
  background-size: cover;
  padding: 60px 0;
}

.cta h3 {
  color: #fff;
  font-size: 28px;
  font-weight: 700;
}

.cta p {
  color: #fff;
}

.cta .cta-btn {
  font-family: "Raleway", sans-serif;
  text-transform: uppercase;
  font-weight: 500;
  font-size: 16px;
  letter-spacing: 1px;
  display: inline-block;
  padding: 8px 28px;
  border-radius: 4px;
  transition: 0.5s;
  margin-top: 10px;
  border: 2px solid #fff;
  color: #fff;
}

.cta .cta-btn:hover {
  background: #206bfb;
  border-color: #206bfb;
  color: #fff!important;
}
</style>