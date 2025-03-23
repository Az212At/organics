<script lang="ts" setup="">
import FooterColumn from "@/components/FooterColumn.vue";

defineOptions({
  name: "TheFooter",
});

const contacts = [
  { text: "P +64 9555 555", href: "#" },
  { text: "F +64 9555 555", href: "#" },
  { text: "E info@email.com", href: "#" },
];

const footerLinks = [
  {
    title: "Services",
    links: [
      "Commercial",
      "Distribution",
      "Gas",
      "Generation",
      "Industrial",
      "Telecomms",
      "Transmission",
      "Water",
    ],
  },
  {
    title: "Markets",
    links: [
      "Commercial",
      "Industrial",
      "Infrastructure",
      "Resources",
      "Utilities",
    ],
  },
  {
    title: "HSEQ",
    links: ["Health & Safety", "Environment", "Quality"],
  },
  {
    title: "About",
    links: ["History", "Structure", "People", "CSR", "Locations", "PPV"],
  },
  {
    title: "Careers",
    links: [
      "Who we are",
      "Benefits",
      "Programmes",
      "Our People",
      "Roles",
      "Vacancies",
    ],
  },
];
</script>

<template>
  <footer class="the-footer">
    <div class="the-footer__container">
      <div class="the-footer__content">
        <div class="the-footer__left-column">
          <h3 class="the-footer__title">Address:</h3>
          <a href="#" class="the-footer__link">http://www.lipsum.com</a>
          <ul class="the-footer__list">
            <li
              v-for="contact in contacts"
              :key="contact.text"
              class="the-footer__list-item"
            >
              <a :href="contact.href" class="the-footer__link">{{
                contact.text
              }}</a>
            </li>
          </ul>
        </div>

        <div class="the-footer__right-column">
          <FooterColumn
            v-for="category in footerLinks"
            :key="category.title"
            :title="category.title"
            :links="category.links"
          />
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
$footer-bg-color: #e56c69;
$text-color: #ffffff;
$link-hover: underline;
$padding-y: 100px 0;
$gap: 75px;

.the-footer {
  padding: $padding-y 0;
  background-color: $footer-bg-color;

  &__container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 15px;
  }

  &__content {
    display: flex;
    justify-content: space-between;
  }

  &__left-column {
    width: 140px;
    height: 144px;
  }

  &__title {
    font-size: 18px;
    line-height: 1;
    color: $text-color;
    margin-bottom: 15px;
  }

  &__link {
    font-size: 14px;
    line-height: 1;
    display: block;
  }

  &__list {
    margin-top: 25px;
  }

  &__right-column {
    display: flex;
    width: 705px;
    height: 250px;
  }

  &__list-item {
    font-size: 14px;
    line-height: 1;
    margin-bottom: 15px;

    &:last-child {
      margin-bottom: 0;
    }
  }

  &__link {
    color: $text-color;
    text-decoration: none;

    &:hover {
      text-decoration: $link-hover;
    }
  }
}
</style>
