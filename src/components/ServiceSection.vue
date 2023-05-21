<script setup>
  import { ref } from "vue";
  import ModalSection from "./ServiceSection/ModalSection.vue"

  let depositModal= ref(null);
  let footPrintModal= ref(null);

  // electronic waste deposit
  let textModalDeposit = [
    "Lixo eletrônico inclui dispositivos eletrônicos quebrados, antigos ou indesejados, como celulares, computadores, TVs, eletrodomésticos, baterias e outros aparelhos eletrônicos. Esse tipo de lixo merece uma atenção especial, então vale a pena entender como descartá-los.",
    "Esses pontos são geralmente locais específicos onde você pode deixar seus dispositivos eletrônicos para descarte adequado. Isso pode incluir lojas, empresas de reciclagem ou eventos especiais de coleta.",
    "A destinação correta do lixo eletrônico é de extrema importância para a preservação do meio ambiente e saúde pública. Além de evitar a contaminação do solo e da água, o descarte adequado dos eletrônicos contribui para a reciclagem de materiais e redução da quantidade de lixo no planeta. Em Franco da Rocha, existem diversos lugares onde é possível realizar o descarte correto do lixo eletrônico, como: "
  ]
  let listModal = [
    {
      title: "Limpe seus dados: ",
      text: "Ao descartar, apague tudo que for possível usando a redefinição de fábrica ou com ferramentas específicas para isso."
    },
    {
      title: "Não jogue no lixo normal: ",
      text: "Nunca coloque o lixo eletrônico no lixo comum ou jogue em qualquer lugar, como no chão ou em rios. Isso pode prejudicar o meio ambiente e a saúde humana devido às substâncias tóxicas que podem ser encontradas neles."
    },
    {
      title: "Procure pontos de coleta: ",
      text: "Verifique se há pontos de coleta de lixo eletrônico perto de sua localidade."
    }
  ]

  let depositAddress = [
    {
      title: "Prefeitura Municipal: ",
      text: "Realiza o descarte de pilhas, baterias, celulares e outros aparelhos eletrônicos.",
      address: "R. Cinco de Maio, 97 - Centro, Franco da Rocha - SP",
      phone: "(11) 4800-1700"
    },
    {
      title: "Etec Franco da Rocha: ",
      text: "Coleta de pilhas, baterias e lâmpadas fluorescentes.",
      address: "Rod. Pref. Luiz Salomão Chamma, 1635 - Pouso Alegre, Franco da Rocha - SP",
      phone: "(11) 4811-7130"
    },
    {
      title: "Fmg Reciclagem de Lixo Eletrônico: ",
      text: "Ccoleta de pilhas e baterias.",
      address: "Rua Ana Sierra Diniz, 415 - Parque Monte Verde, Franco da Rocha - SP",
      phone: "(11) 96438-9780"
    },
    {
      title: "Shopping Franco da Rocha: ",
      text: "O espaço funciona de segunda a sábado, das 9h às 21h e no domingo, das 12h às 20h, e você pode levar o seu 'e-lixo' para ser descartado.",
      address: "Av. dos Expedicionários, 77 - Centro, Franco da Rocha - SP",
      phone: "(11) 4443-0450"
    }
  ]
  
  // footprint calculator
  let textModalFootPrint = [
    "Através do conceito de pegada de carbono, que é a medida total de emissões de gases de efeito estufa resultantes das nossas atividades diárias, podemos analisar o desempenho e o papel crucial na saúde e no futuro do nosso planeta, pelo simples fato do nosso modo de vida. É essencial compreendermos e reduzirmos essa pegada, pois as emissões excessivas estão impulsionando as mudanças climáticas e afetando negativamente o equilíbrio ambiental.",
    "A importância da nossa pegada de carbono reside no fato de que cada ação que tomamos tem um impacto cumulativo no clima global. Desde as escolhas de transporte que fazemos até a energia que consumimos em nossas casas, tudo contribui para a quantidade de dióxido de carbono liberado na atmosfera. Essas emissões, por sua vez, aquecem o planeta, causando alterações climáticas drásticas, como aumento das temperaturas, eventos climáticos extremos e derretimento de geleiras.",
    "Reduzir a nossa pegada de carbono é fundamental para mitigar os impactos adversos das mudanças climáticas. Ao adotarmos práticas sustentáveis, como o uso eficiente de energia, a transição para fontes renováveis, a redução do desperdício e a escolha de dietas mais sustentáveis, podemos diminuir significativamente as emissões e preservar os recursos naturais para as gerações futuras.",
    "Além disso, ao reduzir a nossa pegada de carbono, também estamos abrindo caminho para uma economia mais limpa e sustentável. O investimento em energias renováveis e tecnologias de baixo carbono impulsiona a inovação e cria oportunidades de emprego, ao mesmo tempo em que reduz nossa dependência dos combustíveis fósseis, que são finitos e poluentes.",
    "A conscientização e a ação em relação à nossa pegada de carbono são vitais. Cada um de nós pode fazer a diferença ao fazer escolhas mais sustentáveis e influenciar os outros a seguir o mesmo caminho. Ao assumirmos a responsabilidade por nossas emissões e trabalharmos juntos para reduzi-las, podemos construir um futuro mais saudável e equilibrado para o nosso planeta e todas as formas de vida que nele habitam."
  ]
  
  let footPrintLink = {
    text: "ACESSE AQUI E CALCULE SUA PEGADA",
    link: "https://www.footprintcalculator.org/home/pt"
  }

  function showModal(what){
    if(what === 'depositModal')
      depositModal.value.show();
    else
      footPrintModal.value.show();
  }
</script>

<template>
  <ModalSection 
    ref="depositModal" 
    title="Depósito de Lixo Eletrônico"
    :paragraphs="textModalDeposit"
    :lists="listModal"
    :addresses="depositAddress"
  />

  <ModalSection 
    ref="footPrintModal" 
    title="Calculadora Pegada de Carbono"
    :paragraphs="textModalFootPrint"
    :link="footPrintLink"
  />

    <!-- ======= Services Section ======= -->
    <section id="services" class="services section-bg">
        <div class="container">
            <div class="section-title">
                <span>Serviços</span>
                <h2>Serviços</h2>
                <p>Abaixo estão duas coisas importantes relacionado a TI Verde e Sustentabilidade.</p>
            </div>

            <div class="row justify-content-center">
                <div class="col-lg-4 col-md-6 d-flex align-items-stretch">
                    <div class="icon-box" @click="showModal('depositModal')">
                        <div class="icon"><i class="bi bi-globe-americas"></i></div>
                        <h4>Depósito de Lixo Eletrônico</h4>
                        <p>Clique aqui para acessar informações sobre os locais para depoistar lixo eletrônico</p>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6 d-flex align-items-stretch mt-4 mt-md-0">
                    <div class="icon-box" @click="showModal('footPrintModal')">
                        <div class="icon"><i class='bx bx-fingerprint'></i></div>
                        <h4>Calculadora Pegada de Carbono</h4>
                        <p>Clique aqui para acessar informações sobre a calculadora de pegada de carbono</p>
                    </div>
                </div>
            </div>
        </div>
    </section><!-- End Services Section -->
</template>

<style scoped>
/*--------------------------------------------------------------
# Services
--------------------------------------------------------------*/
.services .icon-box {
  text-align: center;
  border: 1px solid #fff;
  padding: 50px 20px;
  transition: all ease-in-out 0.3s;
  background: #fff;
}

.services .icon-box .icon {
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 20px;
  transition: ease-in-out 0.3s;
}

.services .icon-box .icon i {
  color: #16df7e;
  font-size: 36px;
  transition: 0.3s;
}

.services .icon-box h4 {
  font-weight: 700;
  margin-bottom: 15px;
  font-size: 24px;
  color: #5f687b;
  transition: ease-in-out 0.3s;
}

.services .icon-box p {
  line-height: 24px;
  font-size: 14px;
  margin-bottom: 0;
}

.services .icon-box:hover {
  border-color: #eaecef;
  cursor: pointer;
}

.services .icon-box:hover h4 {
  color: #16df7e;
}
</style>