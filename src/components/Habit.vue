<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <div class="d-flex justify-content-between habit">
          <div class="d-flex stats-container">
            <progress-circle :percentage="25" />
            <div class="habit-name">Run</div>
          </div>
          <div class="sunday">&#10003;</div>
          <div class="monday">&#10003;</div>
          <div class="tuesday">&#10003;</div>
          <div class="wednesday">&#10003;</div>
          <div class="thursday">&#10003;</div>
        </div>
      </div>
    </div>
  </div>

</template>
<script>
  import ProgressCircle from '@/components/ProgressCircle.vue'

export default {
  components: {
    ProgressCircle
  }

}
</script>