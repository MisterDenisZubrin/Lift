<template >
  <button class="button" @click="setFloor"></button>
</template>
<script>
export default {
  props: {
    floorNumber: {
      type: Number,
      required: true
    }
  },
  methods: {
    // @click="addToQueue(floorNumber)"
    // addToQueue(floorNumber) {
    //   // TODO Проверка, что предыдущий этаж не этот же
    //   // Нужно связать с лифтом
    //   this.liftQueue.push(floorNumber);
    // },
    setFloor() {
      const cabin = document.querySelector('.cabin');
      const position = (this.floorNumber * 100) - 100;
      cabin.style.bottom = `${position}px`;
    }
  }
}
</script>
<style lang="scss" scoped>
.button {
  width: 20px;
  height: 20px;
  border: none;
  padding: 0;
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