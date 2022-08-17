<template>
  <a :href="link.link" target="_blank" class="link-component">
    <img :src="`/icons/${link.img}`" alt="" />
    <h3>{{ link.text }}</h3>
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
a {
  width: 100px;
  display: flex;
  flex-direction: column;
  transition: all 150ms;
}

a:hover {
  filter: drop-shadow(3px 5px 2px rgb(0 0 0 / 0.4));
}
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
</style>
