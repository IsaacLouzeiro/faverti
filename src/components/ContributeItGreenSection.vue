<script setup>
  let mainTitle = "Como contribuir com a T.I. Verde?"
  let mainParagraph = "Contribuir com a causa da 'T.I. Verde' envolve adotar práticas e tecnologias sustentáveis na área de Tecnologia da Informação. O objetivo é reduzir o impacto ambiental causado pelo setor, promovendo a eficiência energética, a redução de resíduos eletrônicos e a adoção de soluções mais sustentáveis. Listamos a seguir algumas práticas relacionadas à esse comportamento:"
  let secondParagraph = "Lembrando que essas são apenas algumas das várias maneiras de contribuir com a causa da 'T.I. Verde'. O principal é buscar constantemente soluções mais sustentáveis para minimizar o impacto ambiental da Tecnologia da Informação."

  let items = [
    {
      title: "Eficiência Energética",
      text: "Reduzir o consumo de energia adotando práticas como desligar equipamentos quando não estiverem em uso, configurar computadores para entrar em modo de suspensão, e etc.",
      icon: "bx-plug"
    },
    {
      title: "Virtualização e Consolidação de Servidores",
      text: "Utilize técnicas de virtualização para consolidar vários servidores físicos em um único servidor físico, reduzindo assim o consumo de energia e os recursos necessários.",
      icon: "bx-hdd"
    },
    {
      title: "Computação em Nuvem",
      text: "Considere migrar para serviços de computação em nuvem, que podem ajudar a reduzir o consumo de energia e o desperdício de recursos, permitindo que você utilize apenas os recursos necessários em determinado momento.",
      icon: "bx-cloud"
    },
    {
      title: "Reciclagem e Descarte Adequado de Equipamentos",
      text: "Quando for necessário descartar equipamentos eletrônicos, certifique-se de fazê-lo de forma adequada, seguindo as regulamentações locais e procurando recicladoras especializadas que possam realizar o descarte seguro e a recuperação de materiais.",
      icon: "bx-recycle"
    },
    {
      title: "Redução de Papel",
      text: "Digitalize documentos e adote práticas de trabalho sem papel sempre que possível. Utilize sistemas de gerenciamento eletrônico de documentos e promova a cultura de compartilhamento de arquivos online.",
      icon: "bx-paper-plane"
    },
    {
      title: "Educação e Conscientização",
      text: "Promova a conscientização sobre a importância da T.I. Verde entre colegas, clientes e parceiros de negócios. Eduque-os sobre as práticas sustentáveis que podem ser adotadas e incentive-os a tomar medidas em prol da sustentabilidade.",
      icon: "bx-book-reader"
    }
  ]
</script>

<template>
    <!-- ======= Info Section ======= -->
    <section class="info">
        <div class="container">

            <div class="row">
              <div class="col-lg-6">
                  <img src="../assets/img/aboutGirl.png" class="img-fluid" alt="">
              </div>
              <div class="col-lg-6 pt-4 pt-lg-0 content">
                  <h3>{{ mainTitle }}</h3>
                  <p class="fst-italic"> {{ mainParagraph }} </p>
                  <ul>
                  <li v-for="item in items" :key="item"><i class="bi bi-check-circle"></i><a href="#contribute-green-it">{{ item.title }}</a></li>
                  </ul>
                  <p>
                  {{ secondParagraph }}
                  </p>
              </div>
            </div>

        </div>
    </section><!-- End Info Section -->

    <!-- ======= Contribute Green IT Section ======= -->
    <section id="contribute-green-it" class="contribute-green-it">
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
.contribute-green-it {
  padding: 0;
}

.contribute-green-it .icon-box {
  padding: 20px;
  color: #5f687b;
  background: #fff;
  border-radius: 4px;
  border: 1px solid #f9f9fa;
  transition: 0.3s;
  height: 100%;
}

.contribute-green-it .icon {
  margin: 0 0 15px 0;
}

.contribute-green-it .icon i {
  color: #16df7e;
  font-size: 36px;
}

.contribute-green-it .title {
  font-weight: 600;
  margin-bottom: 15px;
  font-size: 18px;
}

.contribute-green-it .title a {
  color: #5f687b;
  transition: 0.3s;
}

.contribute-green-it .icon-box:hover {
  border-color: #fff;
}

.contribute-green-it .icon-box:hover .title a {
  color: #16df7e;
}

.contribute-green-it .description {
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