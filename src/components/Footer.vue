<template>
  <div>
    <!-- Footer -->
    <footer id="footer" class="section footer">
      <div class="container">
        <div class="footer-container">
          <div class="footer-center">
            <h3>EXTRAS</h3>
            <a href="#">Brands</a>
            <a href="#">Gift Certificates</a>
            <a href="#">Affiliate</a>
            <a href="#">Specials</a>
          </div>
          <div class="footer-center">
            <h3>INFORMATION</h3>
            <a href="#">About Us</a>
            <a href="#">Privacy Policy</a>
            <a href="#">Terms & Conditions</a>
            <a href="#">Contact Us</a>
          </div>
          <div class="footer-center">
            <h3>MY ACCOUNT</h3>
            <a href="#">My Account</a>
            <a href="#">Order History</a>
            <a href="#">Wish List</a>
            <a href="#">Returns</a>
          </div>
          <div class="footer-center">
            <h3>CONTACT US</h3>
            <div>
              <span>
                <i class="fas fa-map-marker-alt"></i>
              </span>
              160 Kemp House, City Roa, London
            </div>
            <div>
              <span>
                <i class="far fa-envelope"></i>
              </span>
              info@styleest.fashion
            </div>
            <div>
              <span>
                <i class="far fa-paper-plane"></i>
              </span>
              London. Uk
            </div>
          </div>
          
        </div>
        <hr class="line">
        <div class="footer-center">
                 <img src="../assets/whitelogo.png" alt="" class="img-fluid" />
          </div>
      </div>
    </footer>
    <!-- End Footer -->
  </div>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
/* ========= Footer ======== */
.footer {
  background-color: var(--black);
  padding: 6rem 1rem;
  line-height: 3rem;
  width: 100vw;
}

.footer-center span {
  margin-right: 1rem;
}

.footer-container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  color: var(--white);
}

.footer-center a:link,
.footer-center a:visited {
  display: block;
  color: var(--grey2);
  font-size: 1.4rem;
  transition: 0.6s;
}
.line {
  background: white;
  width: 100%;
}
.footer-center a:hover {
  color: var(--white);
}

.footer-center div {
  color: var(--grey2);
  font-size: 1.4rem;
}

.footer-center h3 {
  font-size: 1.8rem;
  font-weight: 400;
  margin-bottom: 1rem;
}

@media only screen and (max-width: 998px) {
  .footer-container {
    grid-template-columns: repeat(2, 1fr);
    row-gap: 2rem;
  }
}

@media only screen and (max-width: 768px) {
  .footer-container {
    grid-template-columns: 1fr;
    row-gap: 2rem;
  }
}

</style>
