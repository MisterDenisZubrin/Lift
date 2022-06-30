<template >
  <div class="floor">
    <!-- TODO Сделать вычисляемую ширину -->
    <div class="floor__shaft-space"></div>
    <LiftButton></LiftButton>
    <!-- TODO Заменить спан на компонент индикатора -->
    <span class="floor__number">{{ floorNumber }}</span>
  </div>
</template>
<script>
import LiftButton from './UI/button.vue'
export default {
  components: { LiftButton },
  props: {
    floorNumber: {
      type: Number,
      required: true
    }
  }
}
</script>
<style lang="scss" scoped>
.floor {
  height: 100px;
  width: 100%;
  border: .5px solid grey;
  box-sizing: border-box;
  display: flex;

  &__shaft-space {
    width: 120px;
    height: 100%;
  }

  &__number {
    position: relative;
    left: -15px;
    top: 5px;
    height: 0;
    width: 0;
  }
}
</style>