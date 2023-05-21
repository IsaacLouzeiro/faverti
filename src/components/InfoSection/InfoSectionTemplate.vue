<script setup>
  defineProps({
    templateId: String,
    img: String,
    mainTitle: String,
    mainParagraph: String,
    secondParagraph: String,
    items: Array
  })
</script>

<template>
    <!-- ======= Info Section ======= -->
    <section class="info">
        <div class="container">

            <div class="row">
              <div class="col-lg-6">
                  <img :src="img" class="img-fluid" alt="">
              </div>
              <div class="col-lg-6 pt-4 pt-lg-0 content">
                  <h3>{{ mainTitle }}</h3>
                  <p class="fst-italic"> {{ mainParagraph }} </p>
                  <ul>
                  <li v-for="item in items" :key="item"><i class="bi bi-check-circle"></i><a :href="`#${templateId}`">{{ item.title }}</a></li>
                  </ul>
                  <p>
                  {{ secondParagraph }}
                  </p>
              </div>
            </div>

        </div>
    </section><!-- End Info Section -->

    <!-- ======= IT Green Section ======= -->
    <section :id="templateId" class="it-green">
        <div class="container">
            <div class="row justify-content-center">
                <div 
                  class="col-lg-5 col-md-6" 
                  v-for="item in items"
                  :key="item"
                  >
                    <div class="icon-box">
                        <div class="icon"><i class="bx" :class="item.icon"></i></div>
                        <h4 class="title">{{ item.title }}</h4>
                        <p class="description">{{ item.text }}</p>
                    </div>
                </div>
            </div>
        </div>
    </section><!-- End IT Green Section -->
</template>

<style scoped>
/*--------------------------------------------------------------
# Green IT
--------------------------------------------------------------*/
.it-green {
  padding: 0;
} 

.it-green div>div {
  margin-top: 2px;
  margin-bottom: 2px;
}

.it-green .icon-box {
  padding: 20px;
  color: #5f687b;
  background: #fff;
  border-radius: 4px;
  border: 1px solid #f9f9fa;
  transition: 0.3s;
  height: 100%;
}

.it-green .icon {
  margin: 0 0 15px 0;
}

.it-green .icon i {
  color: #16df7e;
  font-size: 36px;
}

.it-green .title {
  font-weight: 600;
  margin-bottom: 15px;
  font-size: 18px;
  color: #5f687b;
  transition: 0.3s;
}

.it-green .icon-box:hover {
  border-color: #fff;
}

.it-green .icon-box:hover .title {
  color: #16df7e;
}

.it-green .description {
  line-height: 24px;
  font-size: 14px;
}

/*--------------------------------------------------------------
# info
--------------------------------------------------------------*/
.info {
  padding-bottom: 0;
}

.info .content h3 {
  font-weight: 700;
  font-size: 1.6rem;
  color: #5f687b;
}

.info .content ul {
  list-style: none;
  padding: 0;
}

.info .content ul li {
  padding-bottom: 10px;
}

.info .content ul li a {
  color: #16df7e;
}

.info .content ul i {
  font-size: 20px;
  padding-right: 4px;
  color: #16df7e;
}

.info .content p:last-child {
  margin-bottom: 0;
}
</style>