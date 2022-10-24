<template>
  <div class="home">
    <LogoComponent/>
    <LinkArrowComponent message="click aqui para ir ao conversor de moedas" redirect-to="#convert-currency"/>
  </div>
</template>

<script>
import LinkArrowComponent from '@/components/LinkArrowComponent.vue';
import LogoComponent from '@/components/LogoComponent.vue';

export default {
    name: "HomeView",
    components: {
      LogoComponent,
      LinkArrowComponent
    }
}
</script>

<style scoped>
  .home {
    display: flex;
    height: 100vh;
    width: 100vw;
    flex-direction: column;
    flex-wrap: nowrap;
    justify-content: center;
    align-items: center;
    align-content: center;

    /* margin: 0px;
    background-image: url('../assets/background.svg');
    height: 100vh;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover; */
  }
</style>


