<template>
    <!-- ======= Header ======= -->
    <header id="header" class="fixed-top">
        <div class="container d-flex align-items-center justify-content-between">

        <span class="logo"><a href="#hero" class="nav-link">FaVerTI</a></span>
        <nav id="navbar" class="navbar navbar-expand-lg">
            <span class="logo logo-sm"><a class="nav-link"  href="#hero">FaVerTI</a></span>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <i class="bi bi-list mobile-nav-toggle"></i>
            </button>
            <div id="navbarNav" class="collapse navbar-collapse">
            <ul class="navbar-nav">
                <li><a class="nav-link"  href="#hero">Início</a></li>
                <li></li>
                <li><a class="nav-link" href="#info">TI Verde</a></li>
                <li><a class="nav-link" href="#services">Serviços</a></li>
                <li><a class="nav-link" href="#testimonials">Depoimentos</a></li>
                <li><a class="nav-link" href="#team">Sobre Nós</a></li>
            </ul>
            </div>
        </nav><!-- .navbar -->
        
        </div>
    </header><!-- End Header -->
</template>

<style scoped>

/*--------------------------------------------------------------
# Header
--------------------------------------------------------------*/
#header {
  background: #fff;
  transition: all 0.5s;
  z-index: 997;
  padding: 20px 0;
  box-shadow: 0px 2px 15px rgba(0, 0, 0, 0.1);
  padding: 12px 0;
}

#header .logo.logo-sm {
  display: none;
}

#header .logo {
  font-size: 32px;
  margin: 0;
  padding: 0;
  line-height: 1;
  font-weight: 700;
  letter-spacing: 0.5px;
}

#header .logo a {
  color: #5f687b;
}

@media (max-width: 991px) {
  #header {
    padding: 12px 0;
  }

  #header .logo {
    display: none;
  }

  #header .logo.logo-sm {
    display: block;
  }
}

/*--------------------------------------------------------------
# Navigation Menu
--------------------------------------------------------------*/
/**
* Desktop Navigation 
*/
.navbar {
  padding: 0;
}

.navbar ul {
  margin: 0;
  padding: 0;
  display: flex;
  list-style: none;
  align-items: center;
}

.navbar li {
  position: relative;
}

.navbar a {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px 0 10px 30px;
  font-family: "Raleway", sans-serif;
  font-size: 16px;
  font-weight: 700;
  color: #6a7489;
  white-space: nowrap;
  transition: 0.3s;
}

.navbar a i,
.navbar a:focus i {
  font-size: 12px;
  line-height: 0;
  margin-left: 5px;
}

.navbar a:hover,
.navbar-nav .nav-link.active,
.navbar .active,
.navbar .active:focus,
.navbar li:hover>a {
  color: #16df7e;
}

@media (max-width: 991px) {
  .navbar a {
    padding: 10px 0 10px 0px;
  }
}

/**
* Mobile Navigation 
*/
.mobile-nav-toggle {
  color: #5f687b;
  font-size: 28px;
  cursor: pointer;
  display: none;
  line-height: 0;
  transition: 0.5s;
}

.navbar-toggler {
  display: none;
}

.mobile-nav-toggle.bi-x {
  color: #fff;
}

@media (max-width: 991px) {
  .mobile-nav-toggle, .navbar-toggler {
    display: block;
  }

  .navbar-toggler:focus {
    box-shadow: none !important;
  }

  .navbar ul {
    display: block;
    width: 100%;
  }

  .navbar ul li a {
    display: block;
    text-align: center;
  }
  
  .navbar {
    width: 100%;
  }
}
</style>