<template>
    <!-- ======= Services Section ======= -->
    <section id="services" class="services section-bg">
        <div class="container">
            <div class="section-title">
                <span>Serviços</span>
                <h2>Serviços</h2>
                <p>Sit sint consectetur velit quisquam cupiditate impedit suscipit alias</p>
            </div>

            <div class="row justify-content-center">
                <div class="col-lg-4 col-md-6 d-flex align-items-stretch">
                    <div class="icon-box">
                        <div class="icon"><i class="bi bi-globe-americas"></i></div>
                        <h4><a href="">Deposito de Lixo Eletronico</a></h4>
                        <p>Clique aqui para acessar informaçoes sobre os locais para depoistar lixo eletronico mais perto de voce</p>
                    </div>
                </div>

                <div class="col-lg-4 col-md-6 d-flex align-items-stretch mt-4 mt-md-0">
                    <div class="icon-box">
                        <div class="icon"><i class="bi bi-calculator"></i></div>
                        <h4><a href="">Calculadora pegada de carbono</a></h4>
                        <p>Clique aqui para acessar informacoes sobre a calculadora de pegada de carbono</p>
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
}

.services .icon-box h4 a {
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
}

.services .icon-box:hover h4 a {
  color: #16df7e;
}
</style>