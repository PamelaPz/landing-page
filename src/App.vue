<template>
  <div id="app">
    <div class="menu">
      <img class="logo" src="./assets/img/logo.svg" alt="logo">
      <nav>
        <img class="icon-menu" src="./assets/img/icon-hamburger.svg" alt="logo" @click="openMenu"/>
        <ul class="menu-hamburger">
          <li> <a href="#about">About</a> </li>
          <li> <a href="#services">Services</a> </li>
          <li> <a href="#projects">Projects</a> </li>
          <li> <a href="#contact">Contact</a> </li>
        </ul>
      </nav>
    </div>

    <section class="section" id="about">
      <div class="section-creatives">
        <h1 class="title">We are creatives</h1>
        <div class="arrow-down">
          <img src="./assets/img/icon-arrow-down.svg" alt="arrow-down">
        </div>
      </div>
    </section>
    <section class="section" id="services">
      <div class="section-tranStans">
        <div class="wp-text" id="transform">
         <div class="text-info">
            <h2>Transform your brand</h2>
            <p>We are a full-service creative agency specializing in helping brands grow fast.
            Engage your clients through compelling visuals that do most of the marketing for you.</p>
            <div class="link"><a class="btn-more" href="">Learn more</a></div>
         </div>
        </div>
        <picture class="wp-img" id="egg">
          <source media="(min-width: 375px)" srcset="./assets/img/desktop/image-transform.jpg" />
          <img src="./assets/img/mobile/image-transform.jpg" alt="egg">
        </picture>
      </div>
    </section>
    <section class="section">
      <div class="section-tranStans">
        <div class="wp-text" id="stand">
          <div class="text-info">
            <h2>Stand out to the right audience</h2>
            <p>Using a collaborative formula of designers, researchers, photographers, videographers, and copywriters, we’ll build and extend your brand in digital places.</p>
            <div class="link"><a class="btn-more" href="">Learn more</a></div>
          </div>
        </div>
        <picture class="wp-img" id="cup">
          <source media="(min-width: 375px)" srcset="./assets/img/desktop/image-stand-out.jpg" />
          <img src="./assets/img/mobile/image-stand-out.jpg" alt="cup">
        </picture>
      </div>
    </section>
    <section class="section" id="projects">
      <div class="section-fruits">
        <div class="section-fruits-cereza">
         <div class="wp-text">
            <h2>Graphic design</h2>
            <p>Great design makes you memorable. We deliver artwork that underscores your brand message and captures potential clients’ attention.</p>
         </div>
        </div>
        <div class="section-fruits-orange">
          <div class="wp-text">
            <h2>Photography</h2>
            <p>Increase your credibility by getting the most stunning, high-quality photos that improve your business image.</p>
          </div>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="section-testimonials">
        <h3>Client testimonials</h3>
        <div class="wp-testimonials">
          <div class="testimonial">
            <figure><img src="./assets/img/image-emily.jpg" alt=""></figure>
            <p>We put our trust in Sunnyside and they delivered, making sure our needs were met and deadlines were always hit.</p>
            <h3 class="title-name">Emily R.</h3>
            <p class="carrer">Marketing Director</p>
          </div>

          <div class="testimonial">
            <figure><img src="./assets/img/image-thomas.jpg" alt=""></figure>
            <p>Sunnyside’s enthusiasm coupled with their keen interest in our brand’s success made it a satisfying and enjoyable experience.</p>
            <h3 class="title-name">Thomas S.</h3>
            <p class="carrer">Chief Operating Officer</p>
          </div>

          <div class="testimonial">
            <figure><img src="./assets/img/image-jennie.jpg" alt=""></figure>
            <p>Incredible end result! Our sales increased over 400% when we worked with Sunnyside. Highly recommended!</p>
            <h3 class="title-name">Jennie F.</h3>
            <p class="carrer">Business Owner</p>
          </div>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="section-wrap">
        <picture class="picture">
          <source media="(min-width: 375px)" srcset="./assets/img/desktop/image-gallery-milkbottles.jpg" />
          <img src="./assets/img/mobile/image-gallery-milkbottles.jpg" alt="">
        </picture>
        <picture class="picture">
          <source media="(min-width: 375px)" srcset="./assets/img/desktop/image-gallery-orange.jpg" />
          <img src="./assets/img/mobile/image-gallery-orange.jpg" alt="">
        </picture>
        <picture class="picture">
          <source media="(min-width: 375px)" srcset="./assets/img/desktop/image-gallery-cone.jpg" />
          <img src="./assets/img/mobile/image-gallery-cone.jpg" alt="">
        </picture>
        <picture class="picture">
          <source media="(min-width: 375px)" srcset="./assets/img/desktop/image-gallery-sugarcubes.jpg" />
          <img src="./assets/img/mobile/image-gallery-sugar-cubes.jpg" alt="">
        </picture>
      </div>
    </section>
    <footer class="footer" id="contact">
      <img src="./assets/img/logo-green.svg" alt="logo-green">
      <nav>
        <ul>
          <li> <a>About</a> </li>
          <li> <a>Services</a> </li>
          <li> <a>Projects</a> </li>
        </ul>
      </nav>
      <div class="socials">
        <ul>
          <li><img src="./assets/img/icon-facebook.svg" alt=""></li>
          <li><img src="./assets/img/icon-instagram.svg" alt=""></li>
          <li><img src="./assets/img/icon-twitter.svg" alt=""></li>
          <li><img src="./assets/img/icon-pinterest.svg" alt=""></li>
        </ul>
      </div>
      <div class="sub-footer">
        Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>.
        Coded by <a href="https://github.com/PamelaPz">PamelaPz</a>.
      </div>
    </footer>

  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data () {
    return {
      open: false
    }
  },
  methods: {
    openMenu () {
      this.open = !this.open
      const menu = document.querySelector('.menu-hamburger')
      if (this.open) {
        menu.style.display = 'block'
      } else {
        menu.style.display = 'none'
      }
      console.log(menu)
      console.log(this.open)
    }
  }
}
</script>

<style lang="stylus">
@import "assets/styles/styles.styl";

</style>
