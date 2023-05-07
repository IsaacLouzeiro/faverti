<template>
    <!-- ======= Hero Section ======= -->
    <section id="hero" class="d-flex align-items-center">
        <div class="container">
            <div class="row">
                <div class="col-lg-6 pt-5 pt-lg-0 order-2 order-lg-1 d-flex flex-column justify-content-center">
                <h1>O TI pode ser verde</h1>
                <h2>We are team of talented designers making websites with Bootstrap</h2>
                <div class="d-flex">
                    <a href="#green-it" class="btn-get-started scrollto">Saiba Mais</a>
                </div>
                </div>
                <div class="col-lg-6 order-1 order-lg-2 hero-img">
                <img src="../assets/img/infoBoy.jpg" class="img-fluid animated" alt="">
                </div>
            </div>
        </div>
    </section><!-- End Hero -->
</template>

<style scoped>
/*--------------------------------------------------------------
# Hero Section
--------------------------------------------------------------*/
#hero {
    width: 100%;
    height: 80vh;
    background-color: #f9f9fa;
    padding-top: 82px;
}

#hero h1 {
    margin: 0;
    font-size: 48px;
    font-weight: 700;
    line-height: 56px;
    color: #3e4450;
}

#hero h2 {
    color: #858ea1;
    margin: 10px 0 30px 0;
    font-size: 24px;
}

#hero .btn-get-started {
    font-family: "Raleway", sans-serif;
    font-weight: 500;
    font-size: 16px;
    letter-spacing: 1px;
    display: inline-block;
    padding: 8px 30px 10px 30px;
    border-radius: 4px;
    transition: 0.5s;
    color: #fff;
    background: #16df7e;
    box-shadow: 0 8px 28px rgba(22, 223, 126, 0.45);
}

#hero .btn-get-started:hover {
    background: #206bfb;
    box-shadow: 0 8px 28px rgba(32, 107, 251, 0.45);
}

#hero .animated {
    animation: up-down 2s ease-in-out infinite alternate-reverse both;
}

@media (max-width: 991px) {
    #hero {
        height: 100vh;
    }

    #hero .animated {
        animation: none;
    }

    #hero .hero-img {
        text-align: center;
    }

    #hero .hero-img img {
        width: 50%;
    }
}

@media (max-width: 768px) {
    #hero {
        height: auto;
    }

    #hero h1 {
        font-size: 28px;
        line-height: 36px;
    }

    #hero h2 {
        font-size: 18px;
        line-height: 24px;
        margin-bottom: 30px;
    }

    #hero .hero-img img {
        width: 70%;
    }
}

@media (max-width: 575px) {
    #hero .hero-img img {
        width: 80%;
    }
}

@keyframes up-down {
    0% {
        transform: translateY(10px);
    }

    100% {
        transform: translateY(-10px);
    }
}
</style>