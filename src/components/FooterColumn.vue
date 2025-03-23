<script lang="ts" setup="">
import { PropType } from "vue";

defineProps({
  title: {
    type: String,
    default: "",
  },

  links: {
    type: Array as PropType<string[]>,
    default: () => [],
  },
});

defineOptions({
  name: "FooterColumn",
});
</script>

<template>
  <div class="the-footer__right-column">
    <h3 class="the-footer__title">{{ title }}</h3>
    <ul class="the-footer__list">
      <li v-for="link in links" :key="link" class="the-footer__list-item">
        <a href="#" class="the-footer__link">{{ link }}</a>
      </li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
$text-color: #ffffff;
$link-hover: underline;
$gap: 75px;

.the-footer {
  &__right-column {
    display: flex;
    column-gap: $gap;
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
    margin-top: 15px;
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
