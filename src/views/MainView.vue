<template>
  <div class="main">
    <div class="home">
      <HomeView/>
    </div>
    <div class="convert-currency">
      <ConvertCurrencyView/>
    </div>
  </div>
</template>

<script>
import ConvertCurrencyView from './ConvertCurrencyView.vue';
import LinkArrowComponent from '@/components/LinkArrowComponent.vue';
import LogoComponent from '@/components/LogoComponent.vue';
import HomeView from './HomeView.vue';

export default {
    name: "MainView",
    components: {
      HomeView,
      ConvertCurrencyView,
      LinkArrowComponent,
      LogoComponent
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
  }

  .convert-currency {
    /* padding: 100px 0px 0px 0px; */
    position: absolute;
    height: 100vh;
    width: 100vw;
  }
</style>


