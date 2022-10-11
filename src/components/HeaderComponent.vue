<template>
  <header class="header">
    <div class="header__banner">
      <div class="header__banner__img"></div>
      <div class="header__banner__gradient"></div>
    </div>

    <img
      src="@/assets/tekila-logo.svg"
      class="header__logo"
      alt="logo tekila"
    />
    <ThreeHeader />
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
        <button class="button-primary">Voir une démo</button
        ><button class="button-secondary">Devis gratuit</button>
      </div>
    </div>
  </header>
</template>
<script>
import ThreeHeader from "@/components/ThreeHeader.vue";
export default {
  components: {
    ThreeHeader,
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
  &__banner {
    position: absolute;
    height: 200vh;
    width: 100vw;
    top: 0;
    right: 0;
    z-index: -1;
    &__img {
      width: 100%;
      height: 100%;
      background-size: cover;
      filter: blur(6px);
      background-image: url("@/assets/header.jpg");
    }
    &__gradient {
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      right: 0;
      z-index: 0;
      background: linear-gradient(
        180deg,
        rgba(49, 35, 153, 0) 0%,
        $base-color 100%
      );
    }
  }

  &__logo {
    height: 40px;
  }
  & h1 {
    font-size: 24px;
    font-weight: $slim-weight;
  }

  &__bloc {
    display: flex;
    flex-direction: column;
    gap: $small-gap;

    &__title {
      font-size: 96px;
      font-weight: $slim-weight;
      z-index: 10;
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
    }
  }
}
</style>
