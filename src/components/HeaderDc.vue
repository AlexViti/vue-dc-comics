<template>
  <header>
    <nav class="container flex aling-center">
      <img src="@/assets/img/dc-logo.png" alt="" />
      <ul class="flex align-center">
        <li v-for="(link, index) in links" :key="index">
          <a href="link.href">{{ link.text }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "HeaderDc",
  data() {
    return {
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
ul {
  list-style: none;
  margin-left: auto;

  li {
    text-transform: uppercase;
    display: inline-block;

    & + li {
      margin-left: 0.5em;
    }
  }
}
</style>
