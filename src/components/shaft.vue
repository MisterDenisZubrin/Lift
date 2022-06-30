<template >
  <div class="shaft">
    <cabin></cabin>
  </div>
</template>
<script>
import cabin from './cabin.vue'
export default {
  components: { cabin },
}
</script>
<style lang="scss" scoped>
.shaft {
  width: 100px;
  border: 1px dotted black;
  box-sizing: border-box;
  margin: 0 20px;
  position: relative;
}
</style>