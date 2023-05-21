<script setup>
  const members = [
    {
      name: "Daniel Rodrigues",
      phrase: "desenvolvimento sustentável significa prosperidade globalmente compartilhada e ambientalmente sustentável.",
      composer: "Sachs",
      linkedin: "https://www.linkedin.com/in/daniel-rodrigues-8b0623220/"
    },
    {
      name: "Eduardo Souza",
      phrase: "A Evolução tecnológica só fará sentido se andar de mãos dadas com a natureza.",
      linkedin: "https://www.linkedin.com/in/eduardo-souza-1142aa226"
    },
    {
      name: "Eliezer Barbosa",
      phrase: "Um país que polui, destrói a si mesmo.",
      linkedin: "https://www.linkedin.com/in/eliezer-barbosa-santos-3975b9274/"
    },
    {
      name: "Isaac Louzeiro",
      phrase: "Preservar a natureza é conectar-se com um futuro sustentável.",
      linkedin: "https://www.linkedin.com/in/isaac-louzeiro/"
    },
    {
      name: "Marco Antonio",
      phrase: "Sustentabilidade é suprir as necessidades da geração presente, sem afetar a habilidade das gerações futuras de suprir as suas.",
      composer: "Brundtland",
      linkedin: "https://www.linkedin.com/in/marco-antonio-marques-924537277/"
    },
    {
      name: "Renan Silva",
      phrase: "Preservar o planeta é um dever de todos. Pequenas ações sustentáveis hoje geram grandes impactos positivos amanhã.",
      linkedin: "https://www.linkedin.com/in/renan-silva-b616a9265/"
    }
  ]
</script>

<template>
    <!-- ======= Team Section ======= -->
    <section id="team" class="team section-bg">
      <div class="container">
        <div class="section-title">
          <span>Sobre nós</span>
          <h2>Sobre nós</h2>
          <p>Site desenvolvido para o trabalho de de Fundamentos de TI do 1º semestre de Gestão de TI da Faculdade de Tecnologia de Franco da Rocha. Abaixo estão os integrantes da equipe.</p>
        </div>

        <div class="row  justify-content-around">
          <div 
            class="col-lg-4 col-md-6 d-flex align-items-center"
            v-for="member in members"
            :key="member"
            >
            <div class="member">
              <i class='bx bx-user-pin' ></i>
              <h4>{{ member.name }}</h4>
              <p>
                <i data-v-47c507f7="" class="bi bi-quote"></i>
                {{ member.phrase }}
                <i data-v-47c507f7="" class="bi bi-quote" style="transform: rotate(180deg); display: inline-block;"></i>
                <span v-if="member.composer">- {{ member.composer }}</span>
              </p>
              <div class="social">
                <a :href="member.linkedin" target="_blank"><i class="bi bi-linkedin"></i></a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section><!-- End Team Section -->
</template>

<style scoped>
/*--------------------------------------------------------------
# Team
--------------------------------------------------------------*/
.team .member {
  width: 100%;
  text-align: center;
  margin-bottom: 20px;
  padding: 30px 20px;
  background: #fff;
}

.team .member>i {
  font-size: 2em;
  color: #16df7e;
}

.team .member h4 {
  font-weight: 700;
  margin-bottom: 2px;
  font-size: 18px;
}

.team .member span {
  font-style: italic;
  font-size: 13px;
}

.team .member p {
  padding-top: 10px;
  font-size: 14px;
  font-style: italic;
  color: #aaaaaa;
}

.team .member .social {
  margin-top: 15px;
}

.team .member .social a {
  color: #919191;
  transition: 0.3s;
}

.team .member .social a:hover {
  color: #16df7e;
}

.team .member .social i {
  font-size: 18px;
  margin: 0 2px;
}
</style>