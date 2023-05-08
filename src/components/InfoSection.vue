<template>
    <!-- ======= Green IT Section ======= -->
    <section id="green-it" class="green-it">
        <div class="container">
            <div class="row">
                <div class="col-lg-4 col-md-6">
                    <div class="icon-box">
                        <div class="icon"><i class="bi bi-laptop"></i></div>
                        <h4 class="title"><a href="">Lorem Ipsum</a></h4>
                        <p class="description">Voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident</p>
                    </div>
                </div>
                <div class="col-lg-4 col-md-6 mt-4 mt-md-0">
                    <div class="icon-box">
                        <div class="icon"><i class="bi bi-card-checklist"></i></div>
                        <h4 class="title"><a href="">Dolor Sitema</a></h4>
                        <p class="description">Minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat tarad limino ata</p>
                    </div>
                </div>
                <div class="col-lg-4 col-md-6 mt-4 mt-lg-0">
                    <div class="icon-box">
                        <div class="icon"><i class="bi bi-clipboard-data"></i></div>
                        <h4 class="title"><a href="">Sed ut perspiciatis</a></h4>
                        <p class="description">Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur</p>
                    </div>
                </div>
            </div>
        </div>
    </section><!-- End Green IT Section -->

    <!-- ======= Info Section ======= -->
    <section id="info" class="info">
        <div class="container">

            <div class="row">
                <div class="col-lg-6">
                    <img src="../assets/img/infoGirl.jpg" class="img-fluid" alt="">
                </div>
                <div class="col-lg-6 pt-4 pt-lg-0 content">
                    <h3>Voluptatem dignissimos provident quasi corporis voluptates</h3>
                    <p class="fst-italic">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
                    magna aliqua.
                    </p>
                    <ul>
                    <li><i class="bi bi-check-circle"></i> Ullamco laboris nisi ut aliquip ex ea commodo consequat</li>
                    <li><i class="bi bi-check-circle"></i> Duis aute irure dolor in reprehenderit in voluptate velit</li>
                    <li><i class="bi bi-check-circle"></i> Ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate trideta storacalaperda</li>
                    </ul>
                    <p>
                    Ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
                    velit esse cillum dolore eu fugiat nulla pariatur.
                    </p>
                </div>
            </div>

        </div>
    </section><!-- End Info Section -->
</template>

<style scoped>
/*--------------------------------------------------------------
# Green IT
--------------------------------------------------------------*/
.green-it {
  padding: 0;
}

.green-it .icon-box {
  padding: 20px;
  color: #5f687b;
  background: #fff;
  border-radius: 4px;
  border: 1px solid #f9f9fa;
  transition: 0.3s;
  height: 100%;
}

.green-it .icon {
  margin: 0 0 15px 0;
}

.green-it .icon i {
  color: #16df7e;
  font-size: 36px;
}

.green-it .title {
  font-weight: 600;
  margin-bottom: 15px;
  font-size: 18px;
}

.green-it .title a {
  color: #5f687b;
  transition: 0.3s;
}

.green-it .icon-box:hover {
  border-color: #fff;
}

.green-it .icon-box:hover .title a {
  color: #16df7e;
}

.green-it .description {
  line-height: 24px;
  font-size: 14px;
}

/*--------------------------------------------------------------
# info
--------------------------------------------------------------*/
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