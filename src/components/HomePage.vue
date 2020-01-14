<template>
  <div>
    <div class="container navbar">Navbar</div>
    <header class="container">Header</header>
    <main class="container">
      <div class="flex-container">
        <div class="flex-container__item flex-container__item-image">
          <img class="image"
            src="./../assets/images/main-image.jpg"
            alt="Mobirise Mobile App on the phone"
          />
        </div>
        <div class="flex-container__item flex-container__item-text">Text</div>
      </div>
    </main>
    <footer class="container">Footer</footer>
  </div>
</template>

<script>
export default {
  name: "app",
  components: {}
};
</script >

<style lang='less'>
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
  max-width: 100%;
  background-color: @white;
  border: 1px solid black;
}

.image {
    width: 100%;
    text-align: center;
}

/* контейнер */
.container {
  max-width: 100%;
  padding-right: 15px;
  padding-left: 15px;
  margin-left: auto;
  margin-right: auto;
}

/* flex-контейнер */
.flex-container {
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
