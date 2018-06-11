<template>
  <section id="home">
    <section id="landing-page">
      <img :src="require('./../assets/landing-background.png')" class="image-fullWidth" />
      <img :src="require('./../assets/landing-title.png')" class="image-title" />
    </section>
    <section id="concept-introduction">
      <div class="container-center">
        <img :src="require('./../assets/logo.png')"  alt="" class="image-logo">
        <h1>Une expérience interactive</h1>
        <p>Hodos est une <strong>expérience de lecture interactive</strong> sur tablette accompagnée d’un kit de cartes, destinée aux <strong>enfants de 7 à 9 ans avides d’aventures et de découvertes</strong>.</p>
        <p>Avec Hodos, inspiré par les textes de Muriel Szac, Le feuilleton d’Hermès, partez à la rencontre de personnages mythologiques en suivant le parcours d’Hermès, jeune dieu grec, qui découvre le monde à la manière d’un enfant.</p>
      </div>
    </section>
    <section id="quote">
      <div class="container-center">
        <img :src="require('./../assets/bebe-hermes.png')" class="quote-illustration" />
        <q>Le soleil se levait à peine quand Hermès sortit du ventre de sa mère. Il s'étira, bâilla et sauta aussitôt sur ses pieds. Puis il courut à l'entrée de la grotte où il venait de naître pour admirer le monde. "Comme c'est beau !" murmura-t-il.</q>
      </div>
    </section>
    <section id="concept-introduction">
      <div class="container-center">
        <h1>Une histoire extraordinaire</h1>
        <p>Ce livre, animé du souffle des <strong>mythes fondateurs</strong>, nous convie à une lecture vagabonde : celle par laquelle nous suivons les <strong>mille et un rebondissements d'une histoire</strong> dont notre héros est le fil conducteur.</p>
        <p>Mise à la portée de tous, cette histoire offre des réponses, souvent fabuleuses, aux questions que chaque être humain se pose.</p>
      </div>
    </section>
    <section id="map-introduction">
      <img :src="require('./../assets/map-background.png')" class="image-fullWidth" />
      <div class="map-container">
        <div class="map-wrapper-left">
          <img :src="require('./../assets/map-ipad.png')" class="image-ipad" />
          <div class="container container-left">
            <h1>Un plan évolutif</h1>
            <p><strong>Voyagez avec Hermès au cours de son périple</strong> à travers 26 lieux emblématiques de la Grèce Antique. Les 100 chapitres du récit sont ainsi rattachés à l’un de ces lieux et accessibles depuis un <strong>plan interactif et évolutif</strong>. Au fur et à mesure de l’histoire, débloquez des lieux inédits !</p>
          </div>
        </div>
        <div class="container map-wrapper-right container-right">
          <h1>Des cartes magiques</h1>
          <p>Tout au long de la lecture, vous serez amené à rencontrer des personnages qui vont vous transmettre leurs <strong>traits de caractères et leurs aptitudes</strong> afin de vous permettre de continuer votre chemin. À l’aide de vos cartes  interactives, retrouvez l’aptitude dont vous avez besoin pour aider Hermès et posez la sur votre tablette. <strong>Développez un maximum vos compétences afin de progresser dans l’histoire d’Hermès et évoluer à ses côtés</strong>.</p>
        </div>
      </div>
    </section>
    <section id="card-introduction">
      <img :src="require('./../assets/cards-background.png')" class="image-fullWidth" />
      <img :src="require('./../assets/cards.png')" alt="" class="image-fullWidth card-top">
    </section>
    <section id="story-introduction">
      <div class="container-center">
        <h1>Une bande défilée</h1>
        <p>Hodos est avant tout une <strong>expérience de lecture illustrée</strong> et prenant vie à travers une bande défilée divisée en 100 chapitres.</p>
      </div>
      <img :src="require('./../assets/story-ipad.png')" class="image-ipad" />
    </section>
    <footer id="footer">
      <img :src="require('./../assets/footer-background.png')" class="image-fullWidth desktopImage" />
      <img :src="require('./../assets/footer-background-mobile.png')" class="image-fullWidth mobileImage" />
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
export default {
  name: 'App'
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
    font-size: 28px;
    font-weight: 400
  }
  p {
    font-size: 13px;
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
    color: #00194d;
  }

  #quote {
    margin-top: 150px;
    text-align: center;
    .container-center {
      margin: 0 auto;
      q {
        font-size: 20px;
        color: #4ca3ba
      }
    }

    .quote-illustration {
      display: block;
      width: 80%;
      max-width: 200px;
      margin: 0 auto;
    }
  }

  #concept-introduction {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 100px;
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

  #story-introduction {
    position: relative;
    z-index: 3;
    .image-ipad {
      margin: 0 auto;
      max-width: 80vw;
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
      max-width: 500px;
      &-center {
        max-width: 500px;
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
  }
</style>
