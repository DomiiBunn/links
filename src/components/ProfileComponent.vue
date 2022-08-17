<template>
  <div class="profile-component">
    <div class="picture"><img src="/profile.png" /></div>
    <h2>DomiiBunns Links</h2>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.profile-component {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  .picture {
    height: 150px;
    width: 150px;
    border-radius: 100%;
    background-color: rgb(88, 15, 88);
    display: flex;
    justify-content: center;
    align-items: center;
    img {
      height: 140px;
      width: 140px;
      background-color: white;
      border-radius: 50%;
    }
  }
}
</style>
