<template>
  <div class="logo-component">
    <h1>logc</h1>
    <img src="../assets/icon-currency.png" alt="">
    <h1>rrency</h1>
  </div>
</template>

<script>
export default {
  name: 'LogoComponent',
  data: () => {
    return {}
  }
}
</script>

<style scoped lang="scss">
  .logo-component {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    align-items: baseline;
    justify-content: center;
  }

  .logo-component > h1 {
    font-size: 10vw;
  }

  .logo-component > img {
    width: 5vw;
    height: 5vw;
  }
</style>
