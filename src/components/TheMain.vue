<script lang="ts" setup>
defineOptions({
  name: "TheMain",
});

const leftContent =
  "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec leo nisi, feugiat vel placerat vitae,\n" +
  "vulputate ac nibh. Ut scelerisque quis nulla sed tempor. Donec leo nisi, feugiat vel placerat vitae,\n" +
  "vulputate ac nibh. Ut scelerisque quis nulla sed tempor. Donec leo nisi, feugiat vel placerat vitae.";
const rightContent = `Lorem ipsum dolor sit amet, <a href="#">consectetur</a> adipiscing elit. Donec leo nisi, feugiat vel
                    placerat vitae,
                    vulputate ac nibh. Ut scelerisque quis nulla sed tempor. Maecenas viverra leo sed risus laoreet
                    rutrum. Praesent lobortis ultrices vestibulum. <a href="#">Mauris rhoncus sagittis elit</a>, a
                    congue justo eleifend
                    adipiscing. Ut pulvinar dignissim ante, at mollis justo laoreet et. Vestibulum viverra purus ligula,
                    in placerat sapien condimentum nec. In diam nulla, pharetra dapibus molestie vitae, luctus a ante.
                    Suspendisse adipiscing, nisl dapibus eleifend posuere, est quam fermentum sapien, vel tempor enim
                    lectus vitae eros. Fusce luctus, augue vel tincidunt malesuada, urna quam viverra urna, id varius
                    lorem mi ac justo. Cras cursus quam nec diam sollicitudin, in laoreet felis scelerisque. Donec
                    gravida tellus ut placerat gravida. Cras cursus quam nec diam sollicitudin, in laoreet felis
                    scelerisque. Donec gravida tellus ut placerat gravida.`;
</script>

<template>
  <main class="the-main">
    <div class="the-main__container">
      <div class="the-main__content">
        <div class="the-main__left">
          <p class="the-main__left-text">{{ leftContent }}</p>
        </div>

        <div class="the-main__right">
          <h2 class="the-main__right-title">
            Lorem ipsum dolor sit amet consectetur
          </h2>
          <p class="the-main__right-text" v-html="rightContent"></p>
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
$primary-color: #fe992a;
$secondary-color: #737c85;
$border-color: #eaeaea;

$font-size-large: 20px;
$font-size-medium: 14px;
$font-size-title: 24px;

$line-height-large: 1.4;
$line-height-medium: 2;

$left-column-width: 267px;
$right-column-width: 653px;
$padding-main: 100px 0;
$padding-left-column: 39px;

.the-main {
  padding: $padding-main;

  &__container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 15px;
  }

  &__content {
    display: flex;
    justify-content: space-between;
  }

  &__left {
    width: $left-column-width;

    &-text {
      font-size: $font-size-large;
      line-height: $line-height-large;
      color: $primary-color;
      font-style: italic;
    }
  }

  &__right {
    width: $right-column-width;
    padding-left: $padding-left-column;
    border-left: 1px solid $border-color;

    &-title {
      font-size: $font-size-title;
      color: $primary-color;
      margin-bottom: 12px;
    }

    &-text {
      font-size: $font-size-medium;
      line-height: $line-height-medium;
      color: $secondary-color;
    }

    &-link {
      color: $secondary-color;
    }
  }
}
</style>
