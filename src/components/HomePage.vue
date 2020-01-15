<template>
  <div>
    <div class="navbar">
      <a :class="{active: isActive}" @click="isActive=!isActive" href="#">
        <div id="icon-phone" class="navbar__icon navbar__icon-phone"></div>
      </a>
      <a @click="addHighlight" href="#">
        <div id="icon-tablet" class="navbar__icon navbar__icon-tablet"></div>
      </a>
      <a @click="addHighlight" href="#">
        <div id="icon-monitor" class="navbar__icon navbar__icon-monitor"></div>
      </a>
    </div>
    <header class="container">Header</header>
    <main class="container">
      <div class="main">
        <div class="main__item main__item-image">
          <img
            class="image"
            src="./../assets/images/main-image.jpg"
            alt="Mobirise Mobile App on the phone"
          />
        </div>
        <div class="main__item main__item-text">Text</div>
      </div>
    </main>
    <footer class="container">Footer</footer>
  </div>
</template>

<script>
/* eslint-disable no-alert, no-console */

export default {
  name: "app",
  components: {},
  data() {
      return {
          isActive : false,
      }
  },
  methods: {

  }
};
</script >

<style lang='less'>
//icon hover
@gray: #ebebeb;
// navbar, text
@white: #ffffff;
//header, icons
@dark-gray: #2c2c2c;
@bg-color: #f97252;
@max-phone-width: 768px;

header {
  background-color: @dark-gray;
}

footer {
  background-color: @bg-color;
}

.navbar {
  display: -ms-flexbox;
  display: flex;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  max-width: 100%;
  height: 15%;
  background-color: @white;
  border: 1px solid black;

  &__icon {
    height: 60px;
    width: 60px;
    background-repeat: no-repeat;
    background-position: center;

    &:hover, &:active {
      background-color: @gray;
    }

    &-phone {
      background-image: url("data:image/svg+xml,%3Csvg version='1.1' id='Capa_1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink' x='0px' y='0px' width='32px' height='32px' viewBox='0 0 561 561' style='enable-background:new 0 0 561 561;' xml:space='preserve'%3E%3Cg%3E%3Cg id='phone'%3E%3Cpath d='M408,0H153c-28.05,0-51,22.95-51,51v459c0,28.05,22.95,51,51,51h255c28.05,0,51-22.95,51-51V51C459,22.95,436.05,0,408,0z M408,459H153V102h255V459z'/%3E%3C/g%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3C/svg%3E%0A");
    }

    &-tablet {
      background-image: url("data:image/svg+xml,%3Csvg version='1.1' id='Capa_1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink' x='0px' y='0px' width='32px' height='32px' viewBox='0 0 512 512' style='enable-background:new 0 0 512 512;' xml:space='preserve'%3E%3Cg%3E%3Cpath d='M400,0H112C94.4,0,80,14.399,80,32v448c0,17.6,14.399,32,32,32h288c17.6,0,32-14.4,32-32V32C432,14.399,417.6,0,400,0z M256,488.891c-13.746,0-24.891-11.145-24.891-24.891s11.145-24.891,24.891-24.891s24.891,11.145,24.891,24.891 S269.746,488.891,256,488.891z M400,416H112V64h288V416z'/%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3C/svg%3E%0A");
    }

    &-monitor {
      background-image: url("data:image/svg+xml,%3Csvg version='1.1' id='Capa_1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink' x='0px' y='0px' width='32px' height='32px' viewBox='0 0 407.484 407.484' style='enable-background:new 0 0 407.484 407.484;' xml:space='preserve'%3E%3Cpath d='M378.939,16.564H28.544C12.805,16.564,0,29.369,0,45.108v219.985c0,15.739,12.805,28.544,28.544,28.544h131.46 l-7.197,33.431h-24.994c-3.723,0-7.278,1.546-9.818,4.268l-34.512,37c-3.646,3.909-4.627,9.608-2.495,14.51 c2.131,4.902,6.967,8.073,12.313,8.073h220.885c0.006-0.001,0.015-0.001,0.02,0c7.415,0,13.427-6.011,13.427-13.426 c0-3.766-1.55-7.168-4.047-9.606l-34.094-36.551c-2.54-2.723-6.096-4.268-9.818-4.268h-24.994l-7.197-33.431h131.459 c15.74,0,28.545-12.805,28.545-28.544V45.108C407.484,29.369,394.68,16.564,378.939,16.564z M371.242,259.737h-335V50.465h335 V259.737z'/%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3Cg%3E%3C/g%3E%3C/svg%3E%0A");
    }
  }
}

.image {
  width: 100%;
  text-align: center;
}

.container {
  max-width: 100%;
  padding-right: 15px;
  padding-left: 15px;
  margin-left: auto;
  margin-right: auto;
}

.main {
  display: -ms-flexbox;
  display: flex;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
  margin-right: -15px;
  margin-left: -15px;
  background-color: @bg-color;
  justify-content: space-around;

  @media (max-width: @max-phone-width) {
    flex-direction: column;
  }

  &__item {
    &-image {
      background-color: pink;
      flex-basis: 40%;
    }

    &-text {
      background-color: blue;
      flex-basis: 50%;
    }

    @media (max-width: @max-phone-width) {
      -ms-flex: 0 0 100%;
      flex: 0 0 100%;
      max-width: 100%;
    }
  }
}
</style>
