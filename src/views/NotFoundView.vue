<template>
  <div class="not-found">
    <h1>ESSA PÁGINA NÃO EXISTE.</h1>
    <h4>logcurrency</h4>
    <LinkArrowComponent message="click aqui para ir a  página inicia" redirect-to="/"/>
  </div>
</template>

<script>
import LinkArrowComponent from '@/components/LinkArrowComponent.vue';

export default {
  name: 'NotFoundView',
  components: {
    LinkArrowComponent
  }
}
</script>

<style scoped>
  h1 {
    font-size: 5rem;
    margin: 0px;
    text-align-last: center;
  }

  h4 {
    font-size: 1rem;
    margin: 0px;
    text-align-last: center;
  }

  .container-link {
    width: calc(100vw - 40px);
    position: absolute;
    bottom: 0px;
    left: 0px;
    margin: 20px;
  }

  .container-link > a {
    align-items: center;
    text-decoration: none;
    color: white;
    font-size: .8rem;
  }
</style>
