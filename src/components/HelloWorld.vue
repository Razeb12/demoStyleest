<template>
  <div class="hello">
    <!-- Header -->
    <header id="home" class="header">
      <nav class="navigation">
        <div class="nav-center container">
          <div class="logo">
            <img src="../assets/128px-Flag_of_the_United_Kingdom.svg" alt="" class="img-fluid london">
            <h5>English</h5>
          </div>

          <div class="nav-menu">
            <div class="nav-top">
              <div class="logo">
                <a href="#"
                  ><img
                    src="../assets/Logo_FullColor.png"
                    alt=""
                    class="img-fluid"
                /></a>
              </div>
              <div class="close">
                <i class="fas fa-times"></i>
              </div>
            </div>

            <div class="logo1">
              <a href="#"
                ><img
                  src="../assets/Logo_FullColor.png"
                  alt=""
                  class="img-fluid"
              /></a>

            </div>
          </div>

          <div class="nav-icons">
            <span><i class="fas fa-user"></i> Register</span>
            <!-- <span><i class="fas fa-search"></i></span> -->
            <span><i class="fas fa-shopping-basket"></i>Shop</span>
            <span><i class="fa fa-sign-in-alt" aria-hidden="true"></i> Login</span>
          </div>

          <div class="hamburger">
            <i class="fas fa-bars"></i>
          </div>
        </div>
      </nav>
    </header>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  mounted() {
    // Nav
    const nav = document.querySelector(".nav-menu");
    const navigation = document.querySelector(".navigation");
    const openBtn = document.querySelector(".hamburger");
    const closeBtn = document.querySelector(".close");

    const navLeft = nav.getBoundingClientRect().left;
    openBtn.addEventListener("click", () => {
      if (navLeft < 0) {
        navigation.classList.add("show");
        nav.classList.add("show");
        document.body.classList.add("show");
      }
    });

    closeBtn.addEventListener("click", () => {
      if (navLeft < 0) {
        navigation.classList.remove("show");
        nav.classList.remove("show");
        document.body.classList.remove("show");
      }
    });

    // Fixed Nav
    const navBar = document.querySelector(".navigation");
    const navHeight = navBar.getBoundingClientRect().height;
    window.addEventListener("scroll", () => {
      const scrollHeight = window.pageYOffset;
      if (scrollHeight > navHeight) {
        navBar.classList.add("fix-nav");
      } else {
        navBar.classList.remove("fix-nav");
      }
    });

    // Scroll To
    const links = [...document.querySelectorAll(".scroll-link")];
    links.map((link) => {
      link.addEventListener("click", (e) => {
        e.preventDefault();

        const id = e.target.getAttribute("href").slice(1);
        const element = document.getElementById(id);
        const fixNav = navBar.classList.contains("fix-nav");
        let position = element.offsetTop - navHeight;

        if (!fixNav) {
          position = position - navHeight;
        }

        window.scrollTo({
          top: position,
          left: 0,
        });

        navigation.classList.remove("show");
        nav.classList.remove("show");
        document.body.classList.remove("show");
      });
    });

    // preloader
    window.addEventListener("load", () => {
      const loader = document.getElementById("pre-loader");
      setTimeout(() => {
        loader.classList.add("hide");
      }, 2000);
    });

    // PopUp
    const popup = document.querySelector(".popup");
    const closePopup = document.querySelector(".popup-close");

    closePopup.addEventListener("click", () => {
      popup.classList.remove("show");
    });

    window.addEventListener("load", () => {
      setTimeout(() => {
        popup.classList.add("show");
      }, 5000);
    });
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.img-fluid {
  height: 32px;
  margin: 0px auto;
}
.adverts {
  line-height: 3rem;
  height: 3rem;
  background-color: var(--pink);
  text-align: center;
  color: var(--white);
  font-weight: 500;
}
.london {
  height: 20px;
}
.navigation {
  padding: 1.6rem 0;
}

.nav-center {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-top {
  display: none;
}

.logo {
  color: var(--black);
  text-align: center;
}

.nav-icons span {
  border-right: 1px solid gray;
}
.logo span {
  color: var(--pink);
}

.nav-list {
  display: flex;
  align-items: center;
}

.fix-nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1200;
  background-color: var(--white);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.nav-item:not(:last-child) {
  margin-right: 0.5rem;
}

.nav-item {
  padding: 0 1rem;
}

.nav-link {
  position: relative;
  display: inline-block;
  padding: 0.5rem 0 0.2rem;
  font-size: 1.5rem;
  color: var(--black);
  text-transform: uppercase;
  transition: all 500ms ease-in-out;
}

.nav-link::after {
  position: absolute;
  content: "";
  width: 100%;
  height: 2px;
  top: 100%;
  left: 0;
  background: var(--pink);
  transition: transform 0.5s;
  transform: scaleX(0);
  transform-origin: right;
}
.nav-link:hover::after {
  transform: scaleX(1);
  transform-origin: left;
}

.container {
  max-width: 114rem;
  margin: 0 auto;
}
@media only screen and (max-width: 1200px) {
  .container {
    padding: 0 3rem;
  }
}
@media only screen and (max-width: 1200px) {
  .container {
    padding: 0 5rem;
  }
}

.nav-icons span:not(:last-child) {
  margin-right: 0.5rem;
}

.nav-icons span {
  font-size: 1.6rem;
  padding: 0.3rem 0.7rem;
  cursor: pointer;
  transition: all 300ms ease-in-out;
}

.nav-icons .fas {
  transition: all 300ms ease-in-out;
}

.hamburger {
  display: none;
}

@media only screen and (max-width: 996px) {
  .nav-item:not(:last-child) {
    margin-right: 0.3rem;
  }

  .nav-item {
    padding: 0 0.5rem;
  }

  .nav-link {
    font-size: 1.4rem;
  }

  .nav-icons span {
    font-size: 1.2rem;
    padding: 0.3rem 0.7rem;
  }
}

@media only screen and (max-width: 768px) {
  .navigation.show {
    background-color: rgba(0, 0, 0, 0.6);
  }
  .nav-menu {
    position: fixed;
    top: 0;
    left: -100%;
    width: 80%;
    height: 100vh;
    z-index: 9990;
    background-color: var(--white);
    transition: all 500ms linear;
  }

  .nav-menu.show {
    left: 0;
  }
  
  .logo1 {
    display: none;
  }

  .nav-list {
    flex-direction: column;
    align-items: start;
    padding: 2rem 0;
  }

  .nav-menu .logo h1 {
    font-size: 1.8rem;
    font-weight: 500;
    color: var(--white);
  }

  .nav-menu .logo h1 span {
    color: var(--white);
  }

  .nav-top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: var(--pink);
    padding: 1.6rem 2rem;
  }

  .hamburger {
    display: block;
    font-size: 2.5rem;
    cursor: pointer;
  }

  .close {
    font-size: 2rem;
    color: var(--white);
    cursor: pointer;
  }

  .nav-item {
    width: 100%;
    padding: 0;
  }

  .nav-item:not(:last-child) {
    margin-bottom: 1rem;
  }

  .nav-link {
    font-size: 1.8rem;
    width: 100%;
    padding: 1rem 2rem;
  }

  .nav-icons span {
    display: none;
    border: none;
    font-size: 1.6rem;
  }

  .nav-icons span:last-child {
    display: none;
  }

  body.show::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.6);
    z-index: 999;
  }
}
</style>
