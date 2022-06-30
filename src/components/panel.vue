<template>
  <ol class="panel">
    <!-- <span class="indicator" v-for="(floor, index) in floorsNumber">
      {{ index }}
    </span> -->
    <li class="panel__button" v-for="(floor, index) in floorsNumber">
      <LiftButton :floorNumber="index + 1"></LiftButton>
    </li>

  </ol>
</template>
<script>
import LiftButton from './UI/button.vue'
export default {
  components: { LiftButton },
  props: {
    floorsNumber: {
      type: Number,
      required: true
    }
  }
}
</script>
<style lang="scss">
.panel {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column-reverse;
  margin: 0 0 0 20px;
  padding: 0;
  box-sizing: border-box;
  height: 100%;
  justify-content: space-around;

}

</style>