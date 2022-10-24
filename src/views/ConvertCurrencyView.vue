<template>
  <div class="convert-currency" id="convert-currency">
    <div class="container-tittle">
      <a href="/">logcurrency</a>
    </div>
    <div class="container-convert-currency">
      <p>Conversor de moeda</p>
      <div>
        <div>
          <ConvertCurencyComponent/>
        </div>
        <div>
          
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ConvertCurencyComponent from '@/components/ConvertCurencyComponent.vue';

export default {
    name: "ConvertCurrencyView",
    components: {
      ConvertCurencyComponent
    }
}
</script>

<style lang="scss" scoped>

  .convert-currency {
    display: flex;
    flex-direction: column;
    flex-wrap: nowrap;
    align-items: center;
    justify-content: space-evenly;
  }

  p, a {
    margin: 0px;
    font-size: 1.2rem;
    font-weight: 700;
    text-decoration: none;
    color: white;
  }

  .container-tittle {
    width: 90%;
    text-align-last: left;
  }

  .container-convert-currency {
    width: 90%;
    height: 90%;
    border-radius: 15px;
    background-color: white;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    align-content: center;

    p {
      margin: 20px;
      text-align-last: left;
      color: #8B8B8B !important;
    }
    div {
      display: flex;
      width: 90%;
      height: 90%;

      @media (max-width: 1000px) {
        display: flex;
        flex-direction: column;
        align-items: center;
      }
     
      div {
        margin: 10px;
        border: 2px solid #EAEAEA;
        border-radius: 15px;
      }
    }
  }

</style>


