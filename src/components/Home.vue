<template>
  <section id="home">
    <section id="landing-page" class="scrollable">
      <img :src="require('./../assets/landing-background.png')" class="image-fullWidth" />
      <img :src="require('./../assets/landing-title.png')" class="image-title" />
    </section>
    <section id="concept-introduction">
      <div class="container-center">
        <img :src="require('./../assets/logo.png')"  alt="" class="image-logo scrollable scrollable-icon scrollable-absolute">
        <div class="scrollable scrollable-text">
          <h1>Une expérience interactive</h1>
          <p>Hodos est une <strong>expérience de lecture interactive</strong> sur tablette accompagnée d’un kit de cartes, destinée aux <strong>enfants de 7 à 9 ans avides d’aventures et de découvertes</strong>.</p>
          <p>Avec Hodos, inspiré par les textes de Muriel Szac, Le feuilleton d’Hermès, partez à la rencontre de personnages mythologiques en suivant le parcours d’Hermès, jeune dieu grec, qui découvre le monde à la manière d’un enfant.</p>
        </div>
      </div>
    </section>
    <section id="quote">
      <img :src="require('./../assets/Background-introduction.png')"  alt="" class="image-fullWidth">
      <div class="container-center">
        <div class="container-left">
          <div class="scrollable scrollable-text">
            <h1>Une histoire extraordinaire</h1>
            <p>Ce livre, animé du souffle des <strong>mythes fondateurs</strong>, nous convie à une lecture vagabonde : celle par laquelle nous suivons les <strong>mille et un rebondissements d'une histoire</strong> dont notre héros est le fil conducteur.</p>
            <p>Mise à la portée de tous, cette histoire offre des réponses, souvent fabuleuses, aux questions que chaque être humain se pose.</p>
          </div>
        </div>
        <div class="container-right">
          <div class="quote-illustration"></div>
          <!-- <img :src="require('./../assets/bebe-hermes.png')" class="quote-illustration" /> -->
          <div class="scrollable scrollable-text">
            <q>Le soleil se levait à peine quand Hermès sortit du ventre de sa mère. Il s'étira, bâilla et sauta aussitôt sur ses pieds. Puis il courut à l'entrée de la grotte où il venait de naître pour admirer le monde. "Comme c'est beau !" murmura-t-il.</q>
          </div>
        </div>
      </div>
    </section>
    <section id="map-introduction">
      <img :src="require('./../assets/map-background.png')" class="image-fullWidth" />
      <div class="map-container">
        <div class="map-wrapper-left">
          <img :src="require('./../assets/map-ipad.png')" class="image-ipad scrollable scrollable-ipad" />
          <div class="container container-left">
            <div class="scrollable scrollable-text">
              <h1>Un plan évolutif</h1>
              <p><strong>Voyagez avec Hermès au cours de son périple</strong> à travers 26 lieux emblématiques de la Grèce Antique. Les 100 chapitres du récit sont ainsi rattachés à l’un de ces lieux et accessibles depuis un <strong>plan interactif et évolutif</strong>. Au fur et à mesure de l’histoire, débloquez des lieux inédits !</p>
            </div>
          </div>
        </div>
        <div class="container map-wrapper-right container-right">
          <div class="scrollable scrollable-text">
            <h1>Des cartes magiques</h1>
            <p>Tout au long de la lecture, vous serez amené à rencontrer des personnages qui vont vous transmettre leurs <strong>traits de caractères et leurs aptitudes</strong> afin de vous permettre de continuer votre chemin. À l’aide de vos cartes  interactives, retrouvez l’aptitude dont vous avez besoin pour aider Hermès et posez la sur votre tablette. <strong>Développez un maximum vos compétences afin de progresser dans l’histoire d’Hermès et évoluer à ses côtés</strong>.</p>
          </div>
        </div>
      </div>
    </section>
    <section id="card-introduction">
      <img :src="require('./../assets/cards-background.png')" class="image-fullWidth" />
      <img :src="require('./../assets/card-helios.png')" alt="" class="card-helios scrollable scrollable-card scrollable-absolute">
      <img :src="require('./../assets/card-aphrodite.png')" alt="" class="card-aphrodite scrollable scrollable-card scrollable-absolute">
      <img :src="require('./../assets/card-zeus.png')" alt="" class="card-zeus scrollable scrollable-card scrollable-absolute">
      <img :src="require('./../assets/card-artemis.png')" alt="" class="card-artemis scrollable scrollable-card scrollable-absolute">
    </section>
    <section id="story-introduction">
      <div class="container-center">
        <div class="scrollable scrollable-text scrollable-absolute">
          <h1>Une bande défilée</h1>
          <p>Hodos est avant tout une <strong>expérience de lecture illustrée</strong> et prenant vie à travers une bande défilée divisée en 100 chapitres.</p>
        </div>
      </div>
      <!-- <img :src="require('./../assets/story-ipad.png')" class="image-ipad" /> -->
      <div class="scrollable scrollable-ipad-story scrollable-absolute">
        <img :src="require('./../assets/story-ipad-empty.png')" class="image-ipad" />
        <img :src="require('./../assets/ipad-scrollable-story.png')" class="image-ipad-scrolled" />
      </div>
    </section>
    <footer id="footer">
      <img :src="require('./../assets/footer-background.png')" class="image-fullWidth desktopImage  clippedBackground" />
      <img :src="require('./../assets/footer-background-mobile.png')" class="image-fullWidth mobileImage  clippedBackground" />
       <div class="container-center">
        <div class="container-wrapper">
          <a href="#">
            <img :src="require('./../assets/download-appstore.png')" />
          </a>
          <a href="#">
            <img :src="require('./../assets/download-googleplay.png')" />
          </a>
        </div>
        <a href="https://www.gobelins.fr/" target="_blank">
          <img :src="require('./../assets/gobelins-logo.png')" class="footer-logo"/>
        </a>
        <p>Développement - Alexandre Massé &amp; Léa Tanda</p>
        <p>Design - Alix Chabagny &amp; Iris Mangin</p>
      </div>
    </footer>
  </section>
</template>

<script>
import lottie from 'lottie-web'

export default {
  name: 'App',
  data: function () {
    return {
      return () {
        scrollables: []
      }
    }
  },
  methods: {
    onScroll () {
      this.scrollables.forEach((scrollable, index) => {
        let offsetTopY = 0
        let offsetBottomY = 0
        if (scrollable.classList.contains('scrollable-absolute')) {
          const elementbounding = scrollable.getBoundingClientRect()
          offsetBottomY = elementbounding.bottom
          offsetTopY = (elementbounding.top + window.scrollY) - +window.scrollY
        } else {
          offsetBottomY = (scrollable.offsetTop + scrollable.clientHeight) - window.scrollY
          offsetTopY = scrollable.offsetTop - window.scrollY
        }
        const offsetTopYPourcent = offsetTopY / window.innerHeight

        const offsetBottomYPourcent = offsetBottomY / window.innerHeight
        if (offsetBottomYPourcent > 0.5 && offsetBottomYPourcent < 1.5) {
          scrollable.classList.add('isScrolled')
        } else if (scrollable.classList.contains('isScrolled') && (offsetBottomYPourcent < -1 || offsetBottomYPourcent > 3)) {
          scrollable.classList.remove('isScrolled')
        }
        // else if (!this.isScrollingUp && offsetTopYPourcent > 0 && offsetTopYPourcent < 1) {
        //   this.changeStep(index + 1)
        //   this.monthDate = month.getAttribute('data-month-date')
        // }
      })
    }
  },
  mounted () {
    this.scrollables = document.querySelectorAll('.scrollable')
    window.addEventListener('scroll', this.onScroll)
    lottie.loadAnimation({
      container: document.querySelector('.quote-illustration'), // the dom element
      animationData: require('./../assets/animations/hermes-evolution/evolution.json'),
      path: './../assets/animations/hermes-evolution/image',
      renderer: 'svg/canvas/html',
      loop: true,
      autoplay: true,
      rendererSettings: {
        scaleMode: 'noScale',
        clearCanvas: false,
        className: 'some-css-class-name'
      }
    })
  }
}
</script>

<style lang="scss">
  .image {
    display: block;
    &-fullWidth {
      width: 100vw;
      height: auto;
      display: block;
    }
    &-title {
      position: absolute;
      top: 5%;
      left: 50%;
      transform: translateX(-50%);
      width: 150px;
      height: auto,
    }
    &-logo {
      width: 90px;
      margin-left: 20px;
      height: auto;
    }
  }

  .scrollable {
    position: relative;

    &-text {
      opacity: 0;
      transform: translateY(50px);
      transition: transform .7s, opacity 1.5s;
      overflow: hidden;
    }

    &-ipad {
      transform: translateY(30px) rotate(-5deg);
      transition: transform .7s ease-in-out;
    }

    &-icon {
      transform: translateY(-50px) scale(0.5);
      opacity: 0;
      transition: transform .5s, opacity .6s;
    }

    &.isScrolled {
      &.scrollable {
        strong {
          color: #4dc1f7;
        }
        &-text {
          opacity: 1;
          transform: translateY(0);

        }
        &-card {
          transform: translateY(0) translateX(0) rotate(0) scale(1);
        }
        &-ipad {
          transform: translateY(0) rotate(0);
        }
        &-ipad-story {
          .image-ipad-scrolled {
            transform: translateX(-280vw);
          }
        }
        &-icon {
          opacity: 1;
          transform: translateY(0) scale(1);
        }
      }
      &::after {
        transform: translateY(-100%);
      }
    }
  }

  .desktopImage {
    display: none;
  }

  .container {
    &-center {
      padding: 0 20px;
    }
    &-right,
    &-left {
      text-align: left;
    }
  }

  h1, h2, p, q {
    color: #333841;
    opacity: 0.7;
  }

  h1 {
    font-size: 30px;
    font-weight: 400
  }
  p {
    font-size: 18px;
    line-height: 1.7;
  }

  q {
    opacity: 0.4;
    color: #0faa7e;
    font-style: italic;
    font-size: 14px;
    font-weight: 500;
  }

  strong {
    font-weight: 500;
    transition: color .7s;
    color: #333841;
  }

  #landing-page {
    &.scrollable {
      image {
        width: 100%;
        height: 50vw;
        transform: translateY(-10vw);
        transform: scale(1);
      }
      .image-title {
        transform: scale(2) translateX(-25%);
        transition: transform .5s;
      }
    }

    &.isScrolled {
      image {
        transform: translateY(10vw) translateX(-50%);
      }
      .image-title {
        transform: scale(1) translateX(-50%);
      }
    }

  }

  #quote {
    margin-top: -10vw;
    text-align: center;
    .container-center {
      margin: 0 auto;
      max-width: 80%;
      width: 100%;
      display: flex;
      justify-content: center;
      flex-direction: column;

      .container-left,
      .container-right {
        max-width: 90%;
      }

      .container-right {
        margin-top: -4vw;
        text-align: right;
        margin-bottom: 10vw;
      }

      .container-left {
        margin-top: 10vw;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
      }
      q {
        font-size: 20px;
        color: #4dc1f7;
        &::before,
        &::after {
          font-size: 40px;
        }
      }
    }

    .quote-illustration {
      position: relative;
      display: block;
      width: 95%;
      height: 300px;
      margin: 0 auto;
    }
  }

  #concept-introduction {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: -10vw;
  }

  #map-introduction {
    margin-top: -15vw;

    .map-container {
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      justify-content: space-around;

      .map-wrapper-left {
        margin-top: -30vw;
        max-width: 80vw;

        .image-ipad {
          width: 100%;
          height: auto;
        }

        .container-left {
          margin-top: 80px;
          margin-left: 30px;
        }
      }
      .map-wrapper-right {
        padding: 0 20px;
        text-align: right;
      }
    }
  }

  #card-introduction {
    margin-top: -20vw;
    position: relative;

    .card-top {
      position: absolute;
      top: -10vw;
    }

  }

  .scrollable-card {
    &.card-helios {
      position: absolute;
      left: 5vw;
      top: -8vw;
      width: 30vw;
      max-width: 500px;
      height: auto;
      transform: translateX(-5vw) translateY(0) rotate(-15deg);
      transition: transform 1s;
    }

    &.card-aphrodite {
      position: absolute;
      left: 30vw;
      top: 15vw;
      width: 25vw;
      max-width: 450px;
      height: auto;
      transform: translateX(-15vw) translateY(-6vw) rotate(-10deg) scale(1.4);
      transition: transform 1s;
    }

    &.card-zeus {
      position: absolute;
      left: 53vw;
      top: 21vw;
      width: 23vw;
      max-width: 400px;
      transform: translateX(-25vw) translateY(-5vw) rotate(-5deg) scale(1.7);
      transition: transform 1s;
    }

    &.card-artemis {
      position: absolute;
      top: 21vw;
      left: 80vw;
      width: 15vw;
      max-width: 300px;
      transform: translateX(-25vw) translateY(-5vw) rotate(-12deg) scale(2.3);
      transition: transform 1s;
    }
  }

  .image-ipad-scrolled {
    position: absolute;
    left: 0;
    top: 0;
    height: 100%;
    width: auto;
    z-index: 1;
    transform: translateX(-10vw);
    transition: transform 6s;
  }

  #story-introduction {
    position: relative;
    z-index: 3;

    .scrollable-ipad-story {
      position: relative;
      height: 45vw;
      width: 58.8vw;
      margin: 100px auto 50px;
      overflow: hidden;
      border-radius: 10Px;
    }

    .image-ipad {
      position: absolute;
      left: 0;
      top: 0;
      right: 0;
      bottom: 0;
      height: 100%;
      width: 100%;
      z-index: 2;
    }

    .container {
      &-center {
        margin: 100px auto 50px;
      }
    }
  }

  #footer {
    position: relative;
    margin-top: -40vw;
    margin-bottom: 0;
    padding-bottom: 0;

    .container-center {
      position: absolute;
      bottom: 10vh;
      bottom: 16vw;
      margin: 0 auto;
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: space-around;
      flex-wrap: wrap;
      flex-direction: column;
      box-sizing: border-box;

      .container-wrapper {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        margin-bottom: 25vw;
      }
    }

    .footer {
      &-logo {
        width: 80px;
      }
    }

    a {
      display: block;
      width: 150px;

      img {
        width: 100%;
      }
    }

    p {
      color: #FFFFFF;
      opacity: 0.7;
      margin: 4px;
      padding: 0;
      font-size: 10px;
    }
  }

  @media screen and (min-width: 600px) {

    .desktopImage {
      display: block;
    }

    .mobileImage {
      display: none;
    }

    .container {
      max-width: 550px;
      &-center {
        max-width: 550px;
      }
    }
     #story-introduction {
      .scrollable-ipad-story {
        border-radius: 35Px;
      }
    }
    #map-introduction {
      .map-container {
        flex-direction: row;
        flex-wrap: wrap;
        .map-wrapper-left {
          margin-top: -30vw;
          // min-width: 500px;
        }
        .map-wrapper-right {
          padding: 0;
          margin-top: 25vw;
          max-width: 420px;
        }
      }
      .container {
        max-width: none;
      }
    }

    #footer {
      .container-center {
        left: 50%;
        width: 100%;
        transform: translateX(-50%);

        .container-wrapper {
          flex-direction: row;
          // justify-content: space-between;
        }
      }
      .footer-logo {
        width: 150px;
        margin-bottom: 30px;
      }
      p {
        font-size: 14px;
      }
    }
  }

  @media screen and (min-width: 800px) {
    .image {
      &-title {
        top: 25%;
        width: 250px;
      }
      &-logo {
        width: 100px;
      }
    }
    .container {
      max-width: 500px;
      &-center {
        max-width: 500px;
      }
    }

    #story-introduction {
      .image-ipad {
        max-width: 800px;
      }
    }

    #footer{
      .container-wrapper {
        width: 100%;
      }
    }

    #concept-introduction {
      height: 50vw;
      margin-top: 0;
    }

    #map-introduction {
      .map-container {
        flex-direction: row;
        .map-wrapper-left {
          margin-top: -30vw;
          max-width: 500px;
        }
        .map-wrapper-right {
          margin-top: 25vw;
          text-align: left;
        }
      }
    }

     #quote {
      .container-center {
        justify-content: space-between;
        flex-direction: row;

        .container-left,
        .container-right {
          max-width: 40%;
        }

        .container-left {
          margin-top: 30vw;
        }
        .container-right {
          text-align: left;
        }
      }
    }
  }
</style>
