<template>
  <footer>
    <div class="container flex">
      <nav>
        <ul v-for="(column, index) in nav" :key="index">
          <h4>{{ column.title }}</h4>
          <li v-for="(link, index) in column.links" :key="index">
            <a :href="link.href">{{ link.text }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </footer>
</template>

<script>
import dcLogoBg from "@/assets/img/dc-logo-bg.png";

export default {
  name: "FooterDc",
  data() {
    return {
      dcLogoBg,
      nav: [
        {
          title: "DC Comics",
          links: [
            {
              href: "#",
              text: "Characters",
            },
            {
              href: "#",
              text: "Comics",
            },
            {
              href: "#",
              text: "Movies",
            },
            {
              href: "#",
              text: "TV",
            },
            {
              href: "#",
              text: "Games",
            },
            {
              href: "#",
              text: "Videos",
            },
            {
              href: "#",
              text: "News",
            },
          ],
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
footer {
  background: url("~@/assets/img/footer-bg.jpg") no-repeat top/cover;

  .container {
    background: url("~@/assets/img/dc-logo-bg.png") no-repeat right/50%;
  }
}
</style>
