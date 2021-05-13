<template>
  <header>
    <h1>Vue - Atividade Prévia</h1>
  </header>
</template>
<script>
export default {
  name: 'Header',
  props: {
    msg: String,
  },
};
</script>
<style lang="scss">
header {
  position: fixed;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: rgba(81, 71, 110, 0.95);
  height: 15vh;

  h1 {
    font-size: 1.2em;
    font-weight: 500;
    text-transform: uppercase;
  }
}
</style>
