<template>
  <div>
    <section class="hero">
      <div class="glide glide1" id="glide1">
        <div class="glide__track" data-glide-el="track">
          <ul class="glide__slides glide__hero">
            <li class="glide__slide">
              <div class="banner">
                <div class="banner-content">
                  <span>New Inspiration 2020</span>
                  <h1>CLOTHING MADE FOR YOU!</h1>
                  <h3>Trending from men and women style collection</h3>
                  <div class="buttons-group">
                    <button>shop women's</button>
                  </div>
                </div>
                <img
                  src="../assets/PhotoRoom-20210213_121200.png"
                  class="special_01"
                  alt=""
                />
              </div>
            </li>

            <li class="glide__slide">
              <div class="banner banner1">
                <div class="banner-content">
                  <span>New Inspiration 2020</span>
                  <h1>CLOTHING MADE FOR YOU!</h1>
                  <h3>Trending from men and women style collection</h3>
                  <div class="buttons-group">
                    <button>shop men's</button>
                  </div>
                </div>
                <img src="../assets/banner_2.png" class="special_02" alt="" />
              </div>
            </li>

            <li class="glide__slide">
              <div class="banner">
                <div class="banner-content">
                  <span>New Inspiration 2020</span>
                  <h1>CLOTHING MADE FOR YOU!</h1>
                  <h3>Trending from men and women style collection</h3>
                  <div class="buttons-group">
                    <button>shop women's</button>
                  </div>
                </div>
                <img src="../assets/banner_3.png" class="special_03" alt="" />
              </div>
            </li>
          </ul>
        </div>

        <!-- Arrows -->
        <div class="glide__arrows" data-glide-el="controls">
          <button class="glide__arrow glide__arrow--left" data-glide-dir="<">
            <i class="fas fa-arrow-left"></i>
          </button>
          <button class="glide__arrow glide__arrow--right" data-glide-dir=">">
            <i class="fas fa-arrow-right"></i>
          </button>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Glide from "@glidejs/glide";
export default {
  name: "Hero",
  mounted() {
    const glide1 = document.getElementById("glide1");
    const glide2 = document.getElementById("glide2");
    const glide3 = document.getElementById("glide3");

    if (glide1)
      new Glide(glide1, {
        type: "carousel",
        startAt: 0,
        autoplay: 3000,
        hoverpause: true,
        perView: 1,
        animationDuration: 800,
        animationTimingFunc: "linear",
      }).mount();

    if (glide2)
      new Glide(glide2, {
        type: "carousel",
        startAt: 0,
        perView: 5,
        hoverpause: false,
        autoplay: 2000,
        animationDuration: 800,
        animationTimingFunc: "cubic-bezier(0.165, 0.840, 0.440, 1.000)",
        breakpoints: {
          1200: {
            perView: 3,
          },
          768: {
            perView: 2,
          },
        },
      }).mount();

    if (glide3) {
      new Glide(glide3, {
        type: "carousel",
        startAt: 0,
        perView: 3,
        rewin: false,
        autoplay: 3000,
        animationDuration: 800,
        animationTimingFunc: "cubic-bezier(0.165, 0.840, 0.440, 1.000)",
        breakpoints: {
          998: {
            perView: 2,
          },
          768: {
            perView: 1,
          },
        },
      }).mount();
    }
  },
};
</script>

<style scoped>
.hero,
.glide__hero,
.banner {
  position: relative;
  height: 100vh;
  width: 100%;
  background-color: var(--grey-alt);
}

.banner img {
  position: absolute;
  bottom: 0;
  width: 100%;
}

.banner img.special_01 {
  width: 85rem;
  right: -5%;
}
.banner img.special_02 {
  width: 85rem;
  right: -10%;
}
.banner img.special_03 {
  width: 85rem;
  right: -10%;
}

.banner-content {
  position: absolute;
  top: 50%;
  transform: translate(25%, -50%);
}

.banner-content span {
  display: inline-block;
  font-size: 1.4rem;
  color: var(--grey);
  margin-bottom: 1rem;
}

.banner-content h1 {
  font-size: 3.5rem;
  font-weight: 500;
  margin-bottom: 1rem;
}

.banner-content h3 {
  font-weight: 400;
  color: var(--grey);
  margin-bottom: 2rem;
}

.buttons-group button {
  display: inline-block;
  background-color: transparent;
  border: 1px solid var(--black);
  outline: none;
  padding: 1.2rem 3rem;
  font-size: 1.6rem;
  text-transform: uppercase;
  font-weight: 500;
  cursor: pointer;
  transition: all 300ms ease-in-out;
}

.buttons-group button:first-child {
  background-color: var(--black);
  color: var(--white);
}

.buttons-group button:first-child:hover {
  background-color: transparent;
  color: var(--black);
}

.buttons-group button:last-child:hover {
  background-color: var(--black);
  color: var(--white);
}

.glide__arrows {
  /* position: absolute; */
  top: 50%;
}

.glide__arrow {
  position: absolute;
  top: 50%;
  background-color: #555;
  border: 1px solid var(--black);
  outline: none;
  padding: 1.1rem 1.5rem;
  border-radius: 50%;
  font-size: 1.6rem;
  color: var(--white);
  visibility: hidden;
  opacity: 0;
  cursor: pointer;
  transition: all 300ms ease-in-out;
}

.glide:hover .glide__arrow {
  visibility: visible;
  opacity: 1;
}

.glide__arrow:hover {
  color: var(--black);
  background-color: transparent;
}

.glide__arrow--left {
  left: 5%;
}

.glide__arrow--right {
  right: 5%;
}

/********Media Queries*******/

@media screen and (min-width: 1920px) {

  .hero,
  .glide__hero,
  .banner {
    position: relative;
    height: 70vh;
    width: 100%;
    background-color: var(--grey-alt);
  }
  .banner-content {
    left: 7%;
  }
  .banner-content h1 {
    font-size: 4.5rem;
    font-weight: 700;
  }
  .banner-content h3 {
    font-size: 1.8rem;
  }
  .banner img.special_01 {
    left: 70%;
    transform: translateX(-50%);
    width: 95rem;
  }

  .banner img.special_02 {
    left: 65%;
    transform: translateX(-50%);
    width: 100rem;
  }
  .banner img.special_03 {
    left: 65%;
    transform: translateX(-50%);
    width: 100rem;
  }
}
@media screen and (min-width: 1840px) {

  .hero,
  .glide__hero,
  .banner {
    position: relative;
    height: 70vh;
    width: 100%;
    background-color: var(--grey-alt);
  }
  .banner-content {
    left: 7%;
  }
  .banner-content h1 {
    font-size: 4.5rem;
    font-weight: 700;
  }
  .banner-content h3 {
    font-size: 1.8rem;
  }
  .banner img.special_01 {
    left: 70%;
    transform: translateX(-50%);
    width: 85rem;
  }

  .banner img.special_02 {
    left: 65%;
    transform: translateX(-50%);
    width: 85rem;
  }
  .banner img.special_03 {
    left: 65%;
    transform: translateX(-50%);
    width: 85rem;
  }
}
@media (min-width: 1366px) and (max-width: 1366px) {
  .banner-content {
    left: 4%;
  }
  .banner-content h1 {
    font-size: 3.5rem;
    font-weight: 700;
  }
  .banner-content h3 {
    font-size: 1.8rem;
  }
}

@media (min-width: 769px) and (max-width: 1024px) {
  .hero,
  .glide__hero,
  .banner {
    position: relative;
    height: 45vh;
    width: 100%;
    background-color: var(--grey-alt);
  }
  .banner img.special_01 {
    left: 75%;
    transform: translateX(-50%);
    width: 60rem;
  }

  .banner img.special_02 {
    left: 75%;
    transform: translateX(-50%);
    width: 60rem;
  }
  .banner img.special_03 {
    left: 75%;
    transform: translateX(-50%);
    width: 60rem;
  }
}

@media only screen and (max-width: 768px) {
  .hero,
  .glide__hero,
  .banner {
    position: relative;
    height: 50vh;
    width: 100%;
    background-color: var(--grey-alt);
  }
  .banner-content {
    width: 90%;
  }
  .banner-content {
    width: 60%;
    position: absolute;
    top: 30%;
    left: 50%;
    text-align: center;
    transform: translate(-50%, -50%);
  }

  .banner img.special_01 {
    left: 50%;
    transform: translateX(-50%);
    width: 40rem;
  }

  .banner img.special_02 {
    left: 50%;
    transform: translateX(-50%);
    width: 40rem;
  }
  .banner img.special_03 {
    left: 55%;
    transform: translateX(-50%);
    width: 40rem;
  }
}

@media only screen and (max-width: 767px) {
  .hero,
  .glide__hero,
  .banner {
    position: relative;
    height: 60vh;
    width: 100%;
    background-color: var(--grey-alt);
  }
  .banner-content {
    width: 90%;
  }
  .banner-content {
    width: 60%;
    position: absolute;
    top: 30%;
    left: 50%;
    transform: translate(-50%, -50%);
  }

  .banner img.special_01 {
    left: 50%;
    transform: translateX(-50%);
    width: 40rem;
  }

  .banner img.special_02 {
    left: 50%;
    transform: translateX(-50%);
    width: 40rem;
  }
  .banner img.special_03 {
    left: 55%;
    transform: translateX(-50%);
    width: 40rem;
  }
}
@media only screen and (max-width: 568px) {
  .banner-content h1 {
    font-size: 3rem;
  }

  .banner-content h3 {
    font-size: 1.5rem;
    margin-bottom: 1.5rem;
  }

  .buttons-group button {
    padding: 1rem 2.5rem;
    font-size: 1.5rem;
  }
}


@media screen and (max-width: 480px) {
  .banner img.special_01 {
    width: 50rem;
    right: 12%;
  }
  .banner img.special_02 {
    width: 85rem;
    right: 12%;
  }
  .banner img.special_03 {
    width: 85rem;
    right: 12%;
  }
}


@media (max-width: 411px) and (max-width: 411px) {
  .banner img.special_01 {
    width: 28rem;
  }
  .banner img.special_02 {
    width: 28rem;
  }
  .banner img.special_03 {
    width: 28rem;
  }
}


@media (min-width: 360px) and (max-width: 360px) {
  .hero,
  .glide__hero,
  .banner {
    position: relative;
    height: 70vh;
    width: 100vw;
    background-color: var(--grey-alt);
  }
  .banner img.special_01 {
    left: 50%;
    transform: translateX(-50%);
    width: 27rem;
  }

  .banner img.special_02 {
    left: 50%;
    transform: translateX(-50%);
    width: 27rem;
  }
  .banner img.special_03 {
    left: 55%;
    transform: translateX(-50%);
    width: 27rem;
  }
}
/* 
.banner-content {
  position: absolute;
  top: 50%;
  left: 10%;
  transform: translate(25%, -50%);
}
.banner img.special_01 {
  width: 85rem;
  right: 12%;
}
.banner img.special_02 {
  width: 85rem;
  right: 12%;
}
.banner img.special_03 {
  width: 85rem;
  right: 12%;
} */
</style>
