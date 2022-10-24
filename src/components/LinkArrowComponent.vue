<template>
  <div class="link-arrow-component">
    <a :href="redirectTo">{{message}}</a>
  </div>
</template>

<script>
export default {
  name: 'LinkArrowComponent',
  props: ['message', 'redirectTo'],
  data: () => {
    return {}
  }
}
</script>

<style scoped lang="scss">
 .link-arrow-component {
    width: calc(100vw - 40px);
    height: 30px;
    position: absolute;
    bottom: 0px;
    left: 0px;
    margin: 20px;
  }

  .link-arrow-component > a {
    align-items: center;
    text-decoration: none;
    color: white;
    font-size: .8rem;
  }
</style>
