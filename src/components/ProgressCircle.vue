<template>

  <svg class="stat-circle" width="25" viewBox="0 0 20 20">
    <circle class="bg" cx="10" cy="10" r="8"/>
    <circle class="progress" ref="prog" cx="10" cy="10" r="8"/>
    <!-- <text x="50%" y="55%">{{ percentage }}%</text> -->
  </svg>

</template>
<script>
export default {
  props: ['percentage'],

  mounted() {
    debugger
    console.log(this.$refs.prog)
    this.$refs.prog.style.strokeDashoffset = -51 -((51 / 100) * parseFloat(this.percentage))
  }
}
</script>
<style lang="scss">
  .stat-circle {
    margin-right: 15px;
    circle.bg {
      fill: none;
      stroke: #f1f1f1;
      stroke-width: 2;
    }
    circle.progress {
      fill: none;
      stroke: #2ecc71;
      stroke-width: 2;
      stroke-dasharray: 51 51;
      stroke-dashoffset: -51;
      // stroke-dashoffset: -51 -((51 / 100) * 75);
      stroke-linecap: round;
    }
    text {
      font-size: 3px;
      text-anchor: middle;
      fill: #555;
    }
}

</style>