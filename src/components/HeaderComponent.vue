<template>
  <header class="header">
    <div class="header__banner">
      <div class="header__banner__img"></div>
      <div class="header__banner__gradient"></div>
    </div>

    <img src="@/assets/tekila-logo.svg" class="header__logo" />

    <div class="header__bloc">
      <h1>FAITES LA<br />DIFFERENCE</h1>
      <h2>
        Votre site web ressemble à tous les autres ? <br />Créons votre site web
        3.0 sur-mesure
      </h2>
      <div class="header__bloc__buttons">
        <button class="button-primary">Voir une démo</button
        ><button class="button-secondary">Devis gratuit</button>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.header {
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
      filter: blur(10px);
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
    font-size: 96px;
    font-weight: $slim-weight;
    z-index: 10;
    font-family: "GoodTimes";
    text-shadow: $text-color 0px 0px 8px;
  }
  & h2 {
    font-size: 24px;
    font-weight: $slim-weight;
  }

  &__bloc {
    display: flex;
    flex-direction: column;
    gap: $small-gap;

    &__buttons {
      display: flex;
      gap: 32px;
    }
  }
}
</style>
