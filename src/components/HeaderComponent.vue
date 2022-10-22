<template>
  <header class="header">
    <img
      src="@/assets/tekila-logo.svg"
      class="header__logo"
      alt="logo tekila"
    />
    <ThreeHeader class="threejs-object" />
    <div class="header__bloc">
      <div class="header__bloc__title">
        <div class="header__bloc__title__wrapper">
          <div class="header__bloc__title__word">
            <span class="header__bloc__title__word__letter">F</span
            ><span class="header__bloc__title__word__letter">A</span
            ><span class="header__bloc__title__word__letter">I</span
            ><span class="header__bloc__title__word__letter">T</span
            ><span class="header__bloc__title__word__letter">E</span
            ><span class="header__bloc__title__word__letter">S</span>
          </div>

          <div class="header__bloc__title__word">
            <span class="header__bloc__title__word__letter">L</span
            ><span class="header__bloc__title__word__letter">A</span>
          </div>
        </div>
        <div class="header__bloc__title__word">
          <span class="header__bloc__title__word__letter">D</span
          ><span class="header__bloc__title__word__letter">I</span
          ><span class="header__bloc__title__word__letter">F</span
          ><span class="header__bloc__title__word__letter">F</span
          ><span class="header__bloc__title__word__letter">é</span
          ><span class="header__bloc__title__word__letter">R</span
          ><span class="header__bloc__title__word__letter">E</span
          ><span class="header__bloc__title__word__letter">N</span
          ><span class="header__bloc__title__word__letter">C</span
          ><span class="header__bloc__title__word__letter">E</span>
        </div>
      </div>
      <h1>
        Votre site web ressemble à tous les autres ? <br />Créons votre site web
        3.0 sur-mesure
      </h1>
      <div class="header__bloc__buttons">
        <a class="button-primary button" href="#">
          Voir une démo
          <SparklesEffect class="sparkles-effect" />
        </a>
        <a class="button-secondary button" href="#">
          Devis gratuit
          <SparklesEffect class="sparkles-effect" />
        </a>
      </div>
    </div>
  </header>
</template>
<script>
import ThreeHeader from "@/components/ThreeHeader.vue";
import SparklesEffect from "@/components/SparklesEffect.vue";
export default {
  components: {
    ThreeHeader,
    SparklesEffect,
  },
};
</script>

<style lang="scss" scoped>
.header {
  position: relative;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  gap: $medium-gap;
  color: $text-color;
  padding: 32px $mobile-padding;

  @media (min-width: $tablet-screen) {
    padding: 64px 128px;
  }

  &__logo {
    height: 40px;
  }
  & h1 {
    font-size: 24px;
    font-weight: $slim-weight;
  }
  .threejs-object {
    width: 500px;
    height: 100%;
    position: absolute;
    right: 0;
    top: 0;
  }
  &__bloc {
    display: flex;
    flex-direction: column;
    gap: $small-gap;
    z-index: 1;

    &__title {
      font-size: 96px;
      font-weight: $slim-weight;
      font-family: "GoodTimes";
      text-shadow: $text-color 0px 0px 8px;

      &__wrapper {
        display: flex;
        gap: 32px;
      }
      &__word {
        display: flex;
        &__letter {
          animation: jump 2s ease-in infinite;
          @for $i from 1 through 10 {
            &:nth-child(#{$i}) {
              animation-delay: 60ms * $i;
            }
          }

          @keyframes jump {
            10% {
              transform: translateY(10px);
            }
          }
        }
      }
    }

    &__buttons {
      display: flex;
      gap: 32px;
      position: relative;

      .button:hover > .sparkles-effect {
        opacity: 1;
        display: block;
      }

      .sparkles-effect {
        display: none;
      }
    }
  }
}
</style>
