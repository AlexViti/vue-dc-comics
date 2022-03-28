<template>
  <nav class="flex">
    <ul class="container flex align-center justify-between">
      <li v-for="(link, index) in links" :key="index" class="flex align-center">
        <img :src="link.img" alt="link.text" />
        <h4>{{ link.text }}</h4>
      </li>
    </ul>
  </nav>
</template>

<script>
import digitalComics from "@/assets/img/buy-comics-digital-comics.png";
import dcMerchandise from "@/assets/img/buy-comics-merchandise.png";
import subscription from "@/assets/img/buy-comics-subscriptions.png";
import shopLocator from "@/assets/img/buy-comics-shop-locator.png";
import powerVisa from "@/assets/img/buy-dc-power-visa.svg";

export default {
  name: "MainNav",
  data() {
    return {
      links: [
        {
          img: digitalComics,
          text: "Digital Comics",
        },
        {
          img: dcMerchandise,
          text: "DC Merchandise",
        },
        {
          img: subscription,
          text: "Subscription",
        },
        {
          img: shopLocator,
          text: "Comic Shop Locator",
        },
        {
          img: powerVisa,
          text: "DC Power Visa",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/styles/partials/variables";

nav {
  background-color: $blue_color;
  height: 200px;
}

li {
  flex-grow: 1;
}

img {
  max-width: 50px;
  max-height: 50px;
}

h4 {
  font-weight: 400;
}
</style>
