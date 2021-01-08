<template>
  <nav>
    <ul>
      <li>
        <a href="#home">Home</a>
      </li>
      <li>
        <a href="#about">About</a>
      </li>
      <li class="photo">
        <img
          src="https://www.ethiobeauty.com/uploads/images/full/Ethio_Beauty_1R9YACBPqaCg6gShSoxycr4lGZYxldOUscshrRSpJTduuloLUk75WDAApjiI1VQ3MLCM1De1C1Aui73Ee5jsA.jpg"
          alt="small-model"
        />
      </li>
      <li>
        <a href="#gallery">Gallery</a>
      </li>
      <li>
        <a href="#contact">Contact</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Nav",
};
</script>

<style scoped>
nav {
  margin: 1.5rem 0;
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
}

nav ul {
  display: flex;
  align-items: center;
  height: 100px;
  justify-content: space-between;
}

nav ul li:not(:last-child) {
  margin-right: 4rem;
}

nav ul li a {
  text-transform: uppercase;
}

nav ul li img {
  width: 80px;
  height: 80px;
  border-radius: 50%;
}
</style>