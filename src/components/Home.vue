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
        <p>Hodos est une expérience de lecture interactive sur tablette accompagnée d’un kit de cartes, destinée aux enfants de 7 à 9 ans avides d’aventures et de découvertes.</p>
        <p>Avec Hodos, inspiré par les textes de Muriel Szac, Le feuilleton d’Hermès, partez à la rencontre de personnages mythologiques en suivant le parcours d’Hermès, jeune dieu grec, qui découvre le monde à la manière d’un enfant.</p>
      </div>
    </section>
    <section id="map-introduction">
      <img :src="require('./../assets/map-background.png')" class="image-fullWidth" />
      <div class="map-container">
        <div class="map-wrapper-left">
          <img :src="require('./../assets/map-ipad.png')" class="image-ipad" />
          <div class="container container-left">
            <h1>Un plan évolutif</h1>
            <p>Voyagez avec Hermès au cours de son périple à travers 26 lieux emblématiques de la Grèce Antique. Les 100 chapitres du récit sont ainsi rattachés à l’un de ces lieux et accessibles depuis un plan interactif et évolutif. Au fur et à mesure de l’histoire, débloquez des lieux inédits !</p>
          </div>
        </div>
        <div class="container map-wrapper-right container-right">
          <h1>Des cartes connectées</h1>
          <p>Tout au long de la lecture, vous serez amené à rencontrer des personnages qui vont vous transmettre leurs traits de caractères et leurs aptitudes afin de vous permettre de continuer votre chemin. À l’aide de vos cartes  interactives, retrouvez l’aptitude dont vous avez besoin pour aider Hermès et posez la sur votre tablette. Collectez un maximum de cartes et de compétences afin de progresser dans l’histoire d’Hermès et évoluer à ses côtés.</p>
        </div>
      </div>
    </section>
    <section id="card-introduction">
      <img :src="require('./../assets/cards-background.png')" class="image-fullWidth" />
    </section>
    <section id="story-introduction">
      <div class="container-center">
        <h1>Une bande défilée</h1>
        <p>Hodos est avant tout une expérience de lecture illustrée et prenant vie à travers une bande défilée divisée en 100 chapitres.</p>
      </div>
      <img :src="require('./../assets/story-ipad.png')" class="image-ipad" />
    </section>
    <footer id="footer">
      <img :src="require('./../assets/footer-background.png')" class="image-fullWidth" />
      <div class="container-center">
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
    }
    &-title {
      position: absolute;
      top: 25%;
      left: 50%;
      transform: translateX(-50%);
      width: 250px;
      height: auto,
    }
    &-logo {
      width: 100px;
      height: auto;
    }
  }

  .container {
    max-width: 500px;
    &-center {
      max-width: 500px;
    }
    &-right,
    &-left {
      text-align: left;
    }
  }

  h1, h2, p {
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

  #concept-introduction {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 50vw;
  }

  #map-introduction {
    margin-top: -15vw;

    .map-container {
      margin: 0 auto;
      display: flex;
      justify-content: space-around;

      .map-wrapper-left {
        margin-top: -30vw;
        max-width: 500px;

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
        margin-top: 25vw;
      }
    }
  }

  #card-introduction {
    margin-top: -20vw;
  }

  #story-introduction {
    position: relative;
    z-index: 3;
    .image-ipad {
      margin: 0 auto;
      max-width: 800px;
    }
    .container {
      &-center {
        margin: 100px auto 50px;
      }
    }
  }

  #footer {
    margin-top: -40vw;
    margin-bottom: 0;
    .container-center {
      position: absolute;
      bottom: 10vh;
    }
  }

</style>
