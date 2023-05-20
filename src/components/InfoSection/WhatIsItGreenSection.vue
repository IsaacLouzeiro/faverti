<script setup>
  let subtitle = "O que é?"
  let mainParagraph = "A TI Verde, ou Tecnologia da Informação Verde, abrange a aplicação de abordagens e tecnologias sustentáveis no campo da tecnologia da informação (TI). Seu objetivo principal é diminuir o impacto ambiental decorrente das atividades de TI, enfatizando a eficiência energética, a preservação de recursos e a sustentabilidade."
  let secondParagraph = "A área de TI é conhecida por consumir uma quantidade considerável de energia elétrica e recursos naturais, como água e materiais de fabricação. A TI Verde busca minimizar esses efeitos negativos por meio de diversas estratégias."
  let thirdParagraph = "Ao adotar práticas de TI Verde, as organizações podem reduzir custos operacionais, minimizar o impacto ambiental e promover uma imagem corporativa mais sustentável. Adicionalmente, a TI Verde contribui para a construção de um futuro mais sustentável, em que a tecnologia é usada de maneira responsável e consciente em relação ao meio ambiente."
</script>

<template>
    <!-- ======= Info Section ======= -->
    <section class="info">
        <div class="container">
            <div class="row align-items-center">
              <div class="col-lg-6">
                  <img src="../../assets/img/aboutBoy.png" class="img-fluid col-10 align-self-center" alt="">
              </div>
              <div class="col-lg-6 pt-4 pt-lg-0 content">
                  <h3>{{ subtitle }}</h3>
                  <p class="fst-italic">{{ mainParagraph }}</p>
                  <p>{{ secondParagraph }}</p>
                  <p>{{ thirdParagraph }}</p>
              </div>
            </div>

        </div>
    </section><!-- End Info Section -->
</template>

<style scoped>
/*--------------------------------------------------------------
# info
--------------------------------------------------------------*/
.info {
  padding: 0;
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