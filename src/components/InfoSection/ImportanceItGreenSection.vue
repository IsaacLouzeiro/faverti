<script setup>
  let mainTitle = "Qual é a importância da T.I. Verde?"
  let mainParagraph = "A TI Verde é importante por diversas razões:"
  let secondParagraph = "Em resumo, a TI Verde promove a sustentabilidade ambiental, reduz os custos operacionais, melhora a imagem corporativa, assegura a conformidade regulatória e impulsiona a inovação."

  let items = [
    {
      title: "Sustentabilidade Ambiental",
      text: "Ajuda a reduzir o impacto ambiental da TI, promovendo o uso eficiente de energia, água e recursos naturais, e incentivando a reciclagem adequada de equipamentos eletrônicos.",
      icon: "bx-leaf"
    },
    {
      title: "Eficiência Energética",
      text: "Busca melhorar o consumo de energia da TI, reduzindo os custos operacionais e diminuindo as emissões de gases de efeito estufa.",
      icon: "bx-plug"
    },
    {
      title: "Redução de Custos",
      text: "Permite economia de recursos financeiros por meio da otimização de recursos e da redução de desperdícios.",
      icon: "bx-line-chart-down"
    },
    {
      title: "Imagem Corporativa Sustentável",
      text: "Demonstra o compromisso da organização com a responsabilidade ambiental, melhorando sua reputação e atraindo clientes que valorizam a sustentabilidade.",
      icon: "bx-buildings"
    },
    {
      title: "Conformidade Regulatória",
      text: "Ajuda as empresas a cumprir regulamentações e políticas ambientais, evitando multas e sanções.",
      icon: "bx-book-content"
    },
    {
      title: "Estímulo à Inovação",
      text: "Impulsiona a inovação tecnológica, levando ao desenvolvimento de soluções mais eficientes e sustentáveis, aumentando a competitividade das organizações.",
      icon: "bx-bulb"
    }
  ]
</script>

<template>
    <!-- ======= Info Section ======= -->
    <section class="info">
        <div class="container">

            <div class="row">
              <div class="col-lg-6">
                  <img src="../../assets/img/importanceGirl.png" class="img-fluid" alt="">
              </div>
              <div class="col-lg-6 pt-4 pt-lg-0 content">
                  <h3>{{ mainTitle }}</h3>
                  <p class="fst-italic"> {{ mainParagraph }} </p>
                  <ul>
                  <li v-for="item in items" :key="item"><i class="bi bi-check-circle"></i><a href="#importance-green-it">{{ item.title }}</a></li>
                  </ul>
                  <p>
                  {{ secondParagraph }}
                  </p>
              </div>
            </div>

        </div>
    </section><!-- End Info Section -->

    <!-- ======= Importance Green IT Section ======= -->
    <section id="importance-green-it" class="importance-green-it">
        <div class="container">
            <div class="row justify-content-center">
                <div 
                  class="col-lg-5 col-md-6" 
                  v-for="item in items"
                  :key="item"
                  >
                    <div class="icon-box">
                        <div class="icon"><i class="bx" :class="item.icon"></i></div>
                        <h4 class="title"><a href="">{{ item.title }}</a></h4>
                        <p class="description">{{ item.text }}</p>
                    </div>
                </div>
            </div>
        </div>
    </section><!-- End Green IT Section -->
</template>

<style scoped>
/*--------------------------------------------------------------
# Green IT
--------------------------------------------------------------*/
.importance-green-it {
  padding: 0;
}

.importance-green-it div>div {
  margin-top: 2px;
  margin-bottom: 2px;
}

.importance-green-it .icon-box {
  padding: 20px;
  color: #5f687b;
  background: #fff;
  border-radius: 4px;
  border: 1px solid #f9f9fa;
  transition: 0.3s;
  height: 100%;
}

.importance-green-it .icon {
  margin: 0 0 15px 0;
}

.importance-green-it .icon i {
  color: #16df7e;
  font-size: 36px;
}

.importance-green-it .title {
  font-weight: 600;
  margin-bottom: 15px;
  font-size: 18px;
}

.importance-green-it .title a {
  color: #5f687b;
  transition: 0.3s;
}

.importance-green-it .icon-box:hover {
  border-color: #fff;
}

.importance-green-it .icon-box:hover .title a {
  color: #16df7e;
}

.importance-green-it .description {
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
  font-size: 32px;
  color: #5f687b;
}

.info .content ul {
  list-style: none;
  padding: 0;
}

.info .content ul li {
  padding-bottom: 10px;
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