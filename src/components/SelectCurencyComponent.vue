<template>
  <div class="select-curency-component">
    <div class="container-input">
      <img :src="currencySelected.iconUrl" alt="">
      <span class="currency-code">{{currencySelected.code}}</span>
      <input 
        class="currency-name" 
        type="text" 
        name="curreny" 
        :value="currencySelected.name" 
        id="" 
        @focus="dropDwonEnabled = true"
        @blur="dropDwonEnabled = false"
      />
    </div>
    <div class="drop-down" :class="[this.dropDwonEnabled ? 'drop-dwon-enabled' : 'drop-dwon-disabled']">
      <div class="list-drop-down">
        <div 
          v-for="currency in currencies" 
          class="item" 
          @mousedown="currencySelected = currency"
          :id="`currency-${currency.code}`"
        >
          <img :src="currency.iconUrl" alt="">
          <span class="currency-code">{{currency.code}}</span>
          <span class="currency-name">{{currency.name}}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SelectCurencyComponent',
  data: () => {
    return {
      dropDwonEnabled: false,
      currencySelected: {
        name: 'Real Brasileiro',
        code: 'BRL',
        iconUrl: 'https://upload.wikimedia.org/wikipedia/commons/thumb/b/b1/Flag_of_Cura%C3%A7ao.svg/20px-Flag_of_Cura%C3%A7ao.svg.png'
      },
      currencies: [
        {
          name: 'Real Parna',
          code: 'BPP',
          iconUrl: 'https://upload.wikimedia.org/wikipedia/commons/thumb/d/d3/Flag_of_Sint_Maarten.svg/22px-Flag_of_Sint_Maarten.svg.png' 
        },
        {
          name: 'Florim',
          code: 'ANG',
          iconUrl: 'https://upload.wikimedia.org/wikipedia/commons/thumb/b/b1/Flag_of_Cura%C3%A7ao.svg/20px-Flag_of_Cura%C3%A7ao.svg.png' 
        }
      ]
    }
  },
  methods: {
    selectedCurrency(currency) {
      console.log(currency)
    }
  }
}
</script>

<style scoped lang="scss">
  .select-curency-component {
    color: black;
  }

  .currency-code {
    margin: 0px 5px;
    font-weight: 700;
    font-size: 1.5rem;
  }

  .currency-name {
    margin-left: 5px;
  }

  img {
    width: 20%;
    height: 50%;
    object-fit: contain;
  }

  .container-input {
    width: 90%;
    height: 50px;
    background-color: #EAEAEA;
    border-radius: 10px;
    padding: 5px;
    box-sizing: border-box;

    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;

    input {
      margin-top: 5px;
      border: none;
      width: 80%;
      outline: none;
      background-color: transparent;
    }
  }

  .drop-down {
    width: 90%;
    background-color: #EAEAEA;
    border-radius: 5px;
    margin-top: 10px;
    height: 90px;
    overflow: auto;
  }


  ::-webkit-scrollbar {
    background-color: #454545;
    width: 5px;
    border-top-right-radius: 5px;
    border-bottom-right-radius: 5px;
  }

  ::-webkit-scrollbar-thumb {
    background-color: #8B8B8B;
    border-radius: 5px;
  }

  .item {
    height: 30px;
    padding: 0px 5px;
    box-sizing: border-box;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
    transition: 0.3s;
    cursor: pointer;
  }

  .item:hover {
    background-color: #D6D6D6;
    padding-left: 7px;
    transition: .3s;
  }

  .drop-dwon-enabled {
    display: block;
  }

  .drop-dwon-disabled {
    display: none;
  }

</style>
