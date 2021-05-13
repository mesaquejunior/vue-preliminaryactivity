<template>
  <footer>
    <p>Facebook Repositories</p>
  </footer>
</template>
<script>
export default {
  name: 'Footer',
  props: {
    msg: String,
  },
};
</script>
<style lang="scss">
footer {
  position: fixed;
  width: 100%;
  bottom: 0;
  height: 5vh;
  background-color: rgba(14, 13, 20, 0.95);
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
