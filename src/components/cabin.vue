<template >
  <div class="cabin"></div>
</template>

<script>
export default {
  data() {
    return {
      previousFloor: 0,
      currentFloor: 1,
      queue: []
    }
  },
  methods: {
    removeFromQueue(floorNumber) {
      this.queue.unshift(floorNumber);
    },
    changeFloor(floorNumber) {
      [this.previousFloor, this.currentFloor] = [this.currentFloor, floorNumber];
      this.removeFromQueue(this.previousFloor);
      // while queue - работает эта функция
    }
  }
}
</script>

<style lang="scss" scoped>
.cabin {
  position: absolute;
  background-color: aqua;
  width: 100%;
  height: 98px;
  bottom: 0;

  transition-duration: 1s;
}
</style>