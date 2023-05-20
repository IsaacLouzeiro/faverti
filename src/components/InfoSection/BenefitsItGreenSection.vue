<script setup>
  let mainTitle = "Quais os benefícios da T.I. Verde?"
  let mainParagraph = "A T.I. verde pode trazer uma série de vantagens e benefícios para sua empresa, através da promoção da eficiência energética, a diminuição do uso de recursos naturais e a adesão de práticas responsáveis com o meio ambiente."
  let secondParagraph = "Esses são alguns dos benefícios que podem ser alcançados pela implementação da T.I. verde dentro de uma organização, contribuindo para promoção da sustentabilidade e preservação do meio ambiente, diminuindo custos e aumentando a reputação de uma empresa."

  let items = [
    {
      title: "Redução das emissões de carbono",
      text: "Ao escolher práticas mais sustentáveis, como a virtualização, é possível reduzir a quantidade de equipamentos, resultando em menor consumo de energia e emissões de poluentes. Isso contribui para a preservação do meio ambiente e promove uma abordagem mais sustentável na área de TI.",
      icon: "bx-world"
    },
    {
      title: "Redução do consumo energético",
      text: "A TI Verde reduz o consumo de energia através da otimização dos sistemas de TI, do uso de hardware eficiente em energia e da implementação de políticas e sistemas de controle de energia e recursos. Isso inclui dispositivos que se desligam automaticamente quando não estão em uso e torneiras com sensores para economia de água, entre outras práticas.",
      icon: "bxs-battery-low"
    },
    {
      title: "Redução de custos e do uso de recursos naturais",
      text: "A implementação de práticas de reciclagem, reutilização e descarte adequados para os eletrônicos, além de práticas que reduzem a necessidades de equipamentos, economia de energia e a optimização dos recursos utilizados contribuem para a redução de custos nas áreas ligadas a T.I.",
      icon: "bx-leaf"
    },
    {
      title: "Melhora a visão dos consumidores com a empresa",
      text: "A adoção de práticas sustentáveis em qualquer área de uma organização, demonstra comprometimento com causa socioambientais, o que melhora a imagem de uma empresa no mundo corporativo e com seus clientes.",
      icon: "bx-line-chart"
    }
  ]
</script>

<template>
    <!-- ======= Info Section ======= -->
    <section class="info">
        <div class="container">

            <div class="row">
                <div class="col-lg-6">
                    <img src="../../assets/img/infoGirl.jpg" class="img-fluid" alt="">
                </div>
                <div class="col-lg-6 pt-4 pt-lg-0 content">
                    <h3>{{ mainTitle }}</h3>
                    <p class="fst-italic"> {{ mainParagraph }} </p>
                    <ul>
                    <li v-for="item in items" :key="item"><i class="bi bi-check-circle"></i><a href="#benefits-green-it">{{ item.title }}</a></li>
                    </ul>
                    <p>
                    {{ secondParagraph }}
                    </p>
                </div>
            </div>

        </div>
    </section><!-- End Info Section -->

    <!-- ======= Benefits Green IT Section ======= -->
    <section id="benefits-green-it" class="benefits-green-it">
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
.benefits-green-it {
  padding: 0;
}

.benefits-green-it div>div {
  margin-top: 2px;
  margin-bottom: 2px;
}

.benefits-green-it .icon-box {
  padding: 20px;
  color: #5f687b;
  background: #fff;
  border-radius: 4px;
  border: 1px solid #f9f9fa;
  transition: 0.3s;
  height: 100%;
}

.benefits-green-it .icon {
  margin: 0 0 15px 0;
}

.benefits-green-it .icon i {
  color: #16df7e;
  font-size: 36px;
}

.benefits-green-it .title {
  font-weight: 600;
  margin-bottom: 15px;
  font-size: 18px;
}

.benefits-green-it .title a {
  color: #5f687b;
  transition: 0.3s;
}

.benefits-green-it .icon-box:hover {
  border-color: #fff;
}

.benefits-green-it .icon-box:hover .title a {
  color: #16df7e;
}

.benefits-green-it .description {
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