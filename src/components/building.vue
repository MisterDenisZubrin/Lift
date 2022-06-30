<template >
  <div class="building">
    <floor 
      v-for="(floor, index) in floorsNumber" 
      :floorNumber="index + 1"
    >
    </floor>
    <div class="lift">
      <shaft v-for="n in lifts"></shaft>
      <panel :floorsNumber="floorsNumber"></panel>
    </div>
  </div>
</template>
<script>
import shaft from './shaft.vue';
import floor from './floor.vue';
import panel from './panel.vue';
export default {
  components: { shaft, panel, floor},
  data() {
    return {
      floorsNumber: 6,
      lifts: 1,
    }
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