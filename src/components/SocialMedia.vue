<template>
  <ul>
    <li name="instagram" v-if="social_media.instagram">
      <a
        :href="'https://instagram.com/' + social_media.instagram"
        rel="noopener noreferrer"
        target="_blank"
      >
        <i class="lab la-instagram" />
      </a>
    </li>
    <li name="twitter" v-if="social_media.twitter">
      <a
        :href="'https://twitter.com/' + social_media.twitter"
        rel="noopener noreferrer"
        target="_blank"
      >
        <i class="lab la-twitter-square" />
      </a>
    </li>
    <li name="snapchat" v-if="social_media.snapchat">
      <a
        :href="'https://snapchat.com/add/' + social_media.snapchat"
        rel="noopener noreferrer"
        target="_blank"
      >
        <i class="lab la-snapchat-square" />
      </a>
    </li>
    <li name="email" v-if="social_media.email">
      <a
        :href="'mailto:' + social_media.email"
        rel="noopener noreferrer"
        target="_blank"
      >
        <i class="las la-envelope-square" />
      </a>
    </li>
  </ul>
</template>

<script>
export default {
  name: "SocialMedia",
  props: ["social_media"],
};
</script>

<style scoped>
ul {
  position: absolute;
  z-index: 3;
  right: 1.5rem;
  top: 50%;
  transform: translateY(-50%);
}

ul li:not(:last-of-type) {
  margin-bottom: 0.2rem;
}

ul li a {
  font-size: 2.5rem;
}
</style>