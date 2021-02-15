<template>
  <div>
    <div class="container-fluid mt-5">
      <div class="row pad">
        <div class="col-md-4 mt-5 pt-5">
          <div class="banner-content">
            <span class="lead">New Inspiration 2020</span>
            <h1 class="title">CLOTHING MADE FOR YOU!</h1>
            <h3 class="text1">Trending from men and women style collection</h3>
            <div class="buttons-group">
              <button>View More</button>
            </div>
          </div>
        </div>
        <div class="col-md-8 mt-5 pt-5">
          <div id="intro">
            <div class="glide">
              <div class="glide__track" data-glide-el="track">
                <div class="glide__slides glide__hero">
                  <div class="glide__slide">
                    <img src="../assets/grid_1.jpg" alt="" class="img-fluid" />
                    <p class="lead1">Lorem Ipsum</p>
                  </div>
                  <div class="glide__slide">
                    <img src="../assets/grid_2.jpg" alt="" class="img-fluid" />
                    <p class="lead1">Lorem Ipsum</p>
                  </div>
                  <div class="glide__slide">
                    <img src="../assets/grid_3.jpg" alt="" class="img-fluid" />
                    <p class="lead1">Lorem Ipsum</p>
                  </div>
                </div>
              </div>
            </div>
            <div class="glide">
              <div class="glide__arrows" data-glide-el="controls">
                <button
                  class="glide__arrow glide__arrow--left"
                  data-glide-dir="<"
                >
                  <i class="fas fa-arrow-left"></i>
                </button>
                <button
                  class="glide__arrow glide__arrow--right"
                  data-glide-dir=">"
                >
                  <i class="fas fa-arrow-right"></i>
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="container-fluid mt-5 pt-5">
      <div class="row">
        <div class="col-md-6 mt-5">
          <img
            src="../assets/woman-5864279_1920.jpg"
            alt=""
            class="img-fluid image"
          />
          <hr class="mt-5" />
          <h3 class="text mt-4">Designers Dress for Women</h3>
          <span class="lead"
            >Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Necessitatibus, quia.</span
          >
        </div>
        <div class="col-md-6 mt-5">
          <img src="../assets/grid_1.jpg" alt="" class="img-fluid" />
          <hr class="mt-5" />
          <h3 class="text mt-4">Stunning Choice</h3>
          <h5 class="lead">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt,
            magni!
          </h5>
        </div>
      </div>
    </div>
    <hr class="mt-5 pt-5" />
    <!-- <ImageGallery/> -->

    <section class="gallary container-fluid mt-5 pt-5">
      <figure class="gallary-item item-1">
        <img src="../assets/grid_1.jpg" alt="" class="gallary-img" />
        <div class="content">
          <h2>Our Popular Products</h2>
          <a href="#">View more</a>
        </div>
      </figure>

      <figure class="gallary-item item-2">
        <img src="../assets/grid_2.jpg" alt="" class="gallary-img" />
        <div class="content">
          <h2>Winter Collections</h2>
        </div>
      </figure>

      <figure class="gallary-item item-3">
        <img src="../assets/grid_3.jpg" alt="" class="gallary-img" />
        <div class="content">
          <h2>Summer Collections</h2>
        </div>
      </figure>

      <figure class="gallary-item item-4">
        <img src="../assets/grid_4.jpg" alt="" class="gallary-img" />
        <div class="content">
          <h2>Up to 70% OFF Spring Sale!</h2>
        </div>
      </figure>
    </section>

    <div class="container-fluid">
      <div class="facility section" id="facility">
        <div class="facility-contianer container">
          <div class="facility-box">
            <div class="facility-icon">
              <i class="fas fa-plane"></i>
            </div>
            <p>SHOP AROUND THE GLOBE</p>
          </div>

          <div class="facility-box">
            <div class="facility-icon">
              <i class="fas fa-credit-card"></i>
            </div>
            <p>100% MONEY BACK GUARANTEE</p>
          </div>

          <div class="facility-box">
            <div class="facility-icon">
              <i class="far fa-credit-card"></i>
            </div>
            <p>MANY PAYMENT GATEWAYS</p>
          </div>

          <div class="facility-box">
            <div class="facility-icon">
              <i class="fas fa-headset"></i>
            </div>
            <p>24/7 ONLINE SUPPORT</p>
          </div>
        </div>
      </div>
    </div>
    <!-- PopUp -->
    <!-- <div class="popup">
      <div class="popup-content">
        <div class="popup-close">
          <i class="fas fa-times"></i>
        </div>
        <div class="popup-left">
          <div class="popup-img">
            <img src="../assets/grid_1.jpg" alt="popup" />
          </div>
        </div>
        <div class="popup-right">
          <div class="right-content">
            <h1>Get Discount <span>30%</span> Off</h1>
            <p>
              Sign up to our Newsletter and save 30% for you next purchase.
            </p>
            <form action="#">
              <input
                type="email"
                placeholder="Enter your email..."
                class="popup-form"
              />
              <a href="#">Subscribe</a>
            </form>
          </div>
        </div>
      </div>
    </div> -->
  </div>
</template>
<script>
// import ImageGallery from '../components/ImageGallery'
import Glide from "@glidejs/glide";
export default {
  // components:{
  //     ImageGallery
  // },
  name: "Main",
  mounted() {
    var glide = new Glide("#intro", {
      type: "carousel",
      perView: 4,
      autoplay: 3500,
      gap: 10,
      focusAt: "center",
      slideWidth: 60,
      breakpoints: {
        1200: {
          perView: 3,
        },
        800: {
          perView: 2,
        },
        480: {
          perView: 1,
        },
      },
    });

    glide.mount();

    // PopUp
    // const popup = document.querySelector(".popup");
    // const closePopup = document.querySelector(".popup-close");

    // closePopup.addEventListener("click", () => {
    //   popup.classList.remove("show");
    // });

    // window.addEventListener("load", () => {
    //   setTimeout(() => {
    //     popup.classList.add("show");
    //   }, 500);
    // });
  },
};
</script>

<style scoped>

img {
  padding: 0 !important;
}
hr {
  width: 100%;
  padding: 0 15px;
  height: 4px;
}
.glide_hero {
  height: 100%;
}
.glide_slide img {
  width: 100%;
}
.glide__arrow {
  position: absolute;
  top: -110px;
  background-color: #555;
  border: 1px solid var(--black);
  outline: none;
  padding: 1rem 0.2rem;
  border-radius: 50%;
  font-size: 1.2rem;
  color: var(--white);
  cursor: pointer;
  transition: all 300ms ease-in-out;
}
.title {
  font-size: 2.6rem;
  font-weight: 700;
}
.lead {
  font-size: 1.7rem;
}
/* 
.image {
    height: 570px;
} */
.lead1 {
  font-size: 1.5rem;
  text-align: center;
  font-weight: 600;
}

.glide__arrow:hover {
  color: var(--white);
}

.glide__arrow--left {
  left: -1%;
}

.glide__arrow--right {
  right: -1%;
}
.text {
  font-size: 2.5rem;
  font-weight: 700;
}
.text1 {
  font-size: 1.6rem;
}
.buttons-group button {
  display: inline-block;
  background-color: transparent;
  border: 1px solid var(--black);
  outline: none;
  padding: 1.2rem 2rem;
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

/* ======== Grid ======= */
.gallary {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  grid-template-rows: repeat(6, 4vw);
  gap: 2rem;
}

.gallary-item {
  overflow: hidden;
  position: relative;
}

.gallary-item::after {
  content: "";
  position: absolute;
  width: 100vw;
  height: 100%;
  top: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.5);
  padding: 0 !important;
}

.gallary-img {
  object-fit: cover;
  height: 100%;
  width: 100%;
  transition: all 500ms linear;
  padding: 0 !important;
}

.gallary-item:hover .gallary-img {
  transform: scale(1.1);
}

.gallary-item .content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 10;
  color: var(--white);
  width: 100%;
  text-align: center;
}

.gallary-item .content h2 {
  font-size: 2rem;
  font-weight: 500;
}

.gallary-item .content a {
  display: inline-block;
  padding: 1rem 1.5rem;
  border: 1px solid var(--white);
  color: var(--white);
  margin-top: 2rem;
  text-decoration: none;
}

.item-1 {
  grid-column-start: 1;
  grid-column-end: 3;
  grid-row-start: 1;
  grid-row-end: 7;
  padding: 0 !important;
}

.item-2 {
  grid-column-start: 3;
  grid-column-end: 5;
  grid-row-start: 1;
  grid-row-end: 4;
  padding: 0 !important;
}
.item-3 {
  grid-column-start: 5;
  grid-column-end: 7;
  grid-row-start: 1;
  grid-row-end: 4;
  padding: 0 !important;
}
.item-4 {
  grid-column-start: 3;
  grid-column-end: 7;
  grid-row-start: 4;
  grid-row-end: 7;
  padding: 0 !important;
}

@media screen and (min-width: 1920px) {
  * {
    padding: 0 12px;
  }
  .glide__arrow {
    top: -150px;
  }
}
@media screen and (min-width: 1366px) {
  * {
    padding: 0 14px;
  }
}
@media only screen and (max-width: 567px) {
  .brands li img {
    height: 9rem;
  }
  * {
    padding: 0;
  }
}

@media only screen and (max-width: 996px) {
  .gallary-item .content h2 {
    font-size: 1.6rem;
  }

  .gallary-item .content a {
    padding: 0.7rem 1.3rem;
    margin-top: 1.5rem;
  }
}

@media only screen and (max-width: 768px) {
  .glide__arrow {
    top: -160px;
    padding: 1rem 1rem;
  }
  * {
    padding: 0;
  }

  .gallary-item .content h2 {
    font-size: 1.4rem;
  }

  .gallary-item .content a {
    padding: 0.4rem 1rem;
    margin-top: 1rem;
  }
}

@media only screen and (max-width: 600px) {
  * {
    padding: 0;
  }
  .gallary {
    grid-template-columns: repeat(6, 1fr);
    grid-template-rows: repeat(20, 4vw);
  }

  .item-1 {
    grid-column-start: 1;
    grid-column-end: 7;
    grid-row-start: 1;
    grid-row-end: 7;
  }

  .item-2 {
    grid-column-start: 1;
    grid-column-end: 7;
    grid-row-start: 7;
    grid-row-end: 11;
  }
  .item-3 {
    grid-column-start: 1;
    grid-column-end: 7;
    grid-row-start: 11;
    grid-row-end: 15;
  }
  .item-4 {
    grid-column-start: 1;
    grid-column-end: 7;
    grid-row-start: 15;
    grid-row-end: 19;
  }
}

.brands li img {
  width: 100%;
  object-fit: contain;
  height: 12rem;
}

.facility {
  background-color: var(--grey-alt);
  padding: 6rem 0 !important;
}

.facility-contianer {
  display: grid;
  align-items: center;
  grid-template-columns: repeat(4, 1fr);
}

.facility-contianer p {
  font-size: 1.4rem !important;
  font-weight: 600;
}

.facility-icon {
  text-align: center;
}

.facility-box {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.facility-icon {
  position: relative;
  display: inline-block;
  width: 8rem;
  height: 8rem;
  border-radius: 50%;
  border: 1.5px solid var(--white);
  z-index: 1;
  margin-bottom: 1.6rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.facility-icon::before {
  content: "";
  position: absolute;
  display: inline-block;
  border-radius: 50%;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  margin: 0.7rem;
  background-color: var(--white);
  z-index: -1;
}

.facility-icon i {
  font-size: 2rem;
  transition: all 500ms ease-in-out;
}

.facility-box:hover i {
  transform: rotateY(180deg);
}

/*
======================
Facility Media Query
======================
*/
@media only screen and (max-width: 998px) {
  .facility-contianer {
    grid-template-columns: 1fr 1fr;
    row-gap: 3rem;
  }
}

@media only screen and (max-width: 568px) {
  .facility-contianer {
    grid-template-columns: 1fr;
  }

  .facility-icon {
    width: 7rem;
    height: 7rem;
    line-height: 8.5rem;
  }

  .facility-contianer p {
    font-size: 1.4rem;
  }
}
</style>
