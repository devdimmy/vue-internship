<template>
  <div class="app">
    <SocialMedia :social_media="data.social_media" />
    <section>
      <h1 v-if="data.name">{{ data.name }}</h1>
      <img src="./assets/model.png" class="model" alt="model" />
      <Nav />
    </section>
  </div>
</template>

<script>
import SocialMedia from "./components/SocialMedia";
import Nav from "./components/Nav";

export default {
  name: "App",
  components: { SocialMedia, Nav },
  data() {
    return {
      data: {
        name: null,
        social_media: Object,
      },
    };
  },
  created() {
    fetch(`https://hirng-x2021.glitch.me/api`)
      .then((res) => res.json())
      .then((data) => {
        this.data = data;
      })
      .catch((error) => {
        console.error(error);
      });
  },
};
</script>

<style>
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

body {
  height: 100vh;
  width: 100vw;
}

body > #app,
body #app > div {
  width: 100%;
  height: 100%;
}

a {
  color: white;
  text-decoration: none;
}

ul {
  list-style: none;
  padding: 0;
}

img {
  max-width: 100%;
}

.app {
  display: grid;
  height: 100vh;
  color: white;
  font-weight: 100;
  place-items: center;
  position: relative;
  font-family: "Montserrat", sans-serif;
  background: linear-gradient(to right, #BD0F4D, #BD0F4D 50%, #CC2964 50%);
}

section {
  height: 100vh;
  width: 100%;
  text-align: center;
  position: relative;
}

section h1 {
  font-size: 1.8rem;
  letter-spacing: 14px;
  margin: 2.2rem 0;
  text-align: center;
}

section .model {
  width: 520px;
  height: 520px;
  position: absolute;
  top: 40%;
  left: 50%;
  transform: translate(-50%, -40%);
  box-shadow: 0px 35px 60px rgba(0, 0, 0, 0.6);
}
</style>

