<template>
  <div id="app">
    <div class="page-content">
      <div class="card">
        <ProfileComponent />
        <div class="listing">
          <LinkComponent v-for="link in links" :link="link" :key="link" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import LinkComponent from "./components/LinkComponent.vue";
import ProfileComponent from "./components/ProfileComponent.vue";
import linksJson from "./links.json";
export default {
  name: "App",
  components: {
    LinkComponent,
    ProfileComponent,
  },
  data() {
    return {
      links: linksJson,
    };
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Dancing+Script&family=Roboto&display=swap");
* {
  box-sizing: border-box;
}

body {
  background-image: radial-gradient(#ffffff 1.5px, transparent 1.5px),
    radial-gradient(#ffffff 1.5px, transparent 1.5px);
  background-size: 43px 43px;
  background-position: 0 0, 21.5px 21.5px;
  background-color: #94396e;
  margin: 0;
  font-family: "Roboto", sans-serif;
}
#app {
  display: flex;
  justify-content: center;
  align-items: center;
}

.listing {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px;
  width: 100%;
  flex-wrap: wrap;
}

.card {
  margin-top: 20px;
  margin-bottom: 20px;
  background-color: whitesmoke;
  width: 70vw;
  border-radius: 15px 0 15px 0;
  border: solid black 3px;
  box-shadow: black 5px 5px 15px;
  padding: 30px;
  max-width: 700px;
}

a,
a:hover,
a:focus,
a:active {
  text-decoration: none;
  color: inherit;
}
</style>
