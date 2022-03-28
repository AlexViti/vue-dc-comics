<template>
  <header>
    <nav class="container flex">
      <img :src="logo" alt="Logo" />
      <ul class="flex align-center">
        <li
          @click.prevent="selectedIndex = index"
          v-for="(link, index) in links"
          :key="index"
          class="flex align-center"
          :class="{
            selected: index == selectedIndex,
          }"
        >
          <a href="link.href">{{ link.text }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
import logo from "@/assets/img/dc-logo.png";

export default {
  name: "HeaderDc",
  data() {
    return {
      logo,
      selectedIndex: 0,
      links: [
        {
          href: "#",
          text: "characters",
        },
        {
          href: "#",
          text: "comics",
        },
        {
          href: "#",
          text: "movies",
        },
        {
          href: "#",
          text: "tv",
        },
        {
          href: "#",
          text: "games",
        },
        {
          href: "#",
          text: "collectables",
        },
        {
          href: "#",
          text: "videos",
        },
        {
          href: "#",
          text: "fans",
        },
        {
          href: "#",
          text: "news",
        },
        {
          href: "#",
          text: "shop",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/styles/partials/variables";

header {
  background-color: white;
  color: black;
}

img {
  margin: 1.3em 0;
  height: 80px;
}

ul {
  margin-left: auto;

  li {
    text-transform: uppercase;
    font-size: 0.8rem;
    font-weight: 500;

    height: 100%;

    $border: 5px solid transparent;
    border-bottom: $border;
    border-top: $border;

    & + li {
      margin-left: 2ch;
    }

    &.selected {
      border-bottom-color: $blue_color;
    }
  }
}
</style>
