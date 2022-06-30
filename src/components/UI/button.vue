<template >
  <button class="button"></button>
</template>
<script>
export default {

}
</script>
<style lang="scss" scoped>
.button {
  width: 20px;
  height: 20px;
  border: none;
  padding: 0;
  margin: 25px 0 0 25px;
  box-sizing: border-box;
  background-color: green;
  cursor: pointer;

  &:hover {
    background-color: aqua;
  }

  &:active {
    background-color: orange;
  }
}
</style>