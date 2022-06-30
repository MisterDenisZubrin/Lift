<template >
  <div class="building">
    <floor 
      v-for="(floor, index) in floorsNumber" 
      :key="floor" 
      :floorNumber="index + 1">
    </floor>
    <div class="lift">
      <shaft></shaft>
    </div>
  </div>
</template>
<script>
import shaft from './shaft.vue';
import floor from './floor.vue';
export default {
  components: { shaft, floor },
  data() {
    return {
      floorsNumber: 9,
      lifts: 1
    }
  },
  methods: {

  }
}
</script>
<style lang="scss" scoped>
.building {
  border: 2px solid black;
  box-sizing: border-box;
  display: flex;
  flex-direction: column-reverse;
  flex-wrap: wrap;
  position: relative;
}

.lift {
  height: 100%;
  position: absolute;
  display: flex;
  flex-wrap: wrap;
}
</style>