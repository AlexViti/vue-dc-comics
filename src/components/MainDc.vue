<template>
  <main>
    <MainJumbo />
    <div class="container flex">
      <h2>Current series</h2>
      <div v-for="(thumb, index) in thumbs" :key="index" class="card">
        <div class="thumb">
          <img :src="thumb.thumb" alt="" />
        </div>
        <h3>{{ thumb.series }}</h3>
      </div>
      <button>Load more</button>
    </div>
    <MainNav />
  </main>
</template>

<script>
import MainJumbo from "./MainJumbo.vue";
import MainNav from "./MainNav.vue";
import thumbs from "../assets/json/dc-comics.json";

export default {
  name: "MainDc",
  data() {
    return {
      thumbs,
    };
  },
  components: {
    MainJumbo,
    MainNav,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/style";

.container {
  flex-wrap: wrap;
  gap: 1rem;
  position: relative;
  padding: 3rem 0;
}

h2 {
  background: $blue-color;
  position: absolute;
  padding: 0.3em 0.8em;
  top: 0;
  z-index: 2;
  transform: translateY(-50%);
}

h3 {
  font-size: 1rem;
  font-weight: 500;
}

.card {
  width: calc(100% / 6 - 1rem);
}

.thumb {
  width: 100%;
  position: relative;

  &::after {
    content: "";
    display: block;
    padding-bottom: 100%;
  }

  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: 0 0;
    position: absolute;
  }
}

button {
  margin: auto;
  background: $blue-color;
  color: white;
  padding: 0.3em 0.8em;
  border: none;
  cursor: pointer;
}
</style>
