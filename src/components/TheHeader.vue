<script lang="ts" setup="">
defineOptions({
  name: "TheHeader",
});

const navLinks = [
  { text: "Commercial", href: "#" },
  { text: "Industrial", href: "#" },
  { text: "Infrastructure", href: "#" },
  { text: "Resources", href: "#" },
];

const description =
  "Trent from punchy pint when lets get some snag. Get a dog up ya moolah piece of piss trent from\n" +
  "punchy slaps. " +
  "Shazza got us some chuck a sickie heaps he hasn't got a kindie. As stands out like\n" +
  "bush telly with as stands out like porky. She'll be right pretty spiffy trent from punchy cab sav.";
</script>

<template>
  <header class="the-header">
    <a href="#" class="logo">
      <img src="@/assets/logo/logo.png" alt="Логотип сайта" />
    </a>

    <div class="container">
      <nav class="nav">
        <a
          v-for="link in navLinks"
          :key="link.text"
          :href="link.href"
          class="nav__link"
        >
          {{ link.text }}
        </a>
      </nav>

      <div class="header-content">
        <h1 class="header-content__title">I want to feel what you wanted</h1>
        <p class="header-content__text">{{ description }}</p>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
$white-link-color: #ffffff;
$nav-margin-bottom: 120px;
$nav-font-size: 30px;
$nav-font-weight: bold;

.the-header {
  padding: 150px 0;
  background-image: url("@/assets/background/header.jpg");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  position: relative;
}

.container {
  width: 960px;
  margin-left: auto;
  margin-right: auto;
}

.logo {
  position: absolute;
  top: 30px;
  left: 30px;
}

.nav {
  display: flex;
  justify-content: space-between;
  margin-bottom: $nav-margin-bottom;

  &__link {
    font-size: $nav-font-size;
    font-weight: $nav-font-weight;
    text-decoration: none;
    color: $white-link-color;

    &:hover {
      text-decoration: underline;
    }
  }
}

.header-content {
  width: 438px;

  &__title {
    font-weight: 400;
    font-size: 52px;
    color: $white-link-color;
    text-shadow: 4px 1px 5px rgba(0, 0, 0, 0.41);
    margin-bottom: 30px;
  }

  &__text {
    font-size: 20px;
    line-height: 1.75;
    color: $white-link-color;
    text-shadow: 0 1px 1px rgba(0, 0, 0, 0.5);
  }
}
</style>
