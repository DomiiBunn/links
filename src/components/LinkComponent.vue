<template>
  <a :href="link.link" target="_blank" class="link-component">
    <img :src="`/icons/${link.img}`" alt="" />
    <h3>{{ link.text }}</h3>
    <p>{{ link.link }}</p>
  </a>
</template>

<script>
export default {
  props: {
    link: Object,
  },
};
</script>

<style lang="scss" scoped>
img {
  height: 100px;
  filter: drop-shadow(3px 5px 2px rgb(0 0 0 / 0.4));
}

.link-component {
  text-shadow: 3px 2px 2px rgb(0 0 0 / 0.4);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

@media only screen and (max-width: 815px) {
  .link-component {
    flex-direction: column;
  }
}
</style>
