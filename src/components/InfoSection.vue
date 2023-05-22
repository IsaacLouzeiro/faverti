<script setup>
  import WhatIsItGreenSection from './InfoSection/WhatIsItGreenSection.vue'
  import InfoSectionTemplate from './InfoSection/InfoSectionTemplate.vue'

  const importanceItGreenList = [
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

  import imgImportance from '@/assets/img/importanceGirl.png'

  const benefitsItGreenList = [
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
  
  import imgBenefits from '@/assets/img/infoGirl.jpg'

  const contributeItGreenList = [
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

  import imgContribute from '@/assets/img/aboutGirl.png'
</script>

<template>
    <!-- ======= Info Section ======= -->
    <section id="info" class="info">
      <div class="section-title">
          <span>TI Verde</span>
          <h2>TI Verde</h2>
      </div>

      <!-- What Is IT Green -->
      <WhatIsItGreenSection />

      <!-- Importance IT Green -->
      <InfoSectionTemplate
        :img="imgImportance"
        mainTitle="Qual é a importância da T.I. Verde?"
        mainParagraph="A TI Verde é importante por diversas razões: "
        secondParagraph="Em resumo, a TI Verde promove a sustentabilidade ambiental, reduz os custos operacionais, melhora a imagem corporativa, assegura a conformidade regulatória e impulsiona a inovação."
        :items="importanceItGreenList"
        templateId="importance-it-green"
      />

      <!-- Benefits IT Green -->
      <InfoSectionTemplate
        :img="imgBenefits"
        mainTitle="Quais os benefícios da T.I. Verde?"
        mainParagraph="A T.I. verde pode trazer uma série de vantagens e benefícios para sua empresa, através da promoção da eficiência energética, a diminuição do uso de recursos naturais e a adesão de práticas responsáveis com o meio ambiente."
        secondParagraph="Esses são alguns dos benefícios que podem ser alcançados pela implementação da T.I. verde dentro de uma organização, contribuindo para promoção da sustentabilidade e preservação do meio ambiente, diminuindo custos e aumentando a reputação de uma empresa."
        :items="benefitsItGreenList"
        templateId="benefits-it-green"
      />

      <!-- Contribute IT Green -->
      <InfoSectionTemplate
        :img="imgContribute"
        mainTitle="Como contribuir com a T.I. Verde?"
        mainParagraph="Contribuir com a causa da 'T.I. Verde' envolve adotar práticas e tecnologias sustentáveis na área de Tecnologia da Informação. O objetivo é reduzir o impacto ambiental causado pelo setor, promovendo a eficiência energética, a redução de resíduos eletrônicos e a adoção de soluções mais sustentáveis. Listamos a seguir algumas práticas relacionadas à esse comportamento:"
        secondParagraph="Lembrando que essas são apenas algumas das várias maneiras de contribuir com a causa da 'T.I. Verde'. O principal é buscar constantemente soluções mais sustentáveis para minimizar o impacto ambiental da Tecnologia da Informação."
        :items="contributeItGreenList"
        templateId="contribute-it-green"
      />
    </section><!-- End Info Section -->
  </template>

<style scoped>

</style>