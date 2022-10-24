<template>
  <div class="convert-curency-component">
    <SelectCurencyComponent/>
  </div>
</template>

<script>
import SelectCurencyComponent from './SelectCurencyComponent.vue';

export default {
  name: 'ConvertCurencyComponent',
  components: {
    SelectCurencyComponent
  },
  data: () => {
    return {}
  }
}
</script>

<style scoped lang="scss">
  .convert-curency-component {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    align-items: baseline;
    justify-content: center;

    border: none !important;
  }
</style>
