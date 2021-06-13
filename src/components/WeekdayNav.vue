<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <div class="d-flex habit justify-content-between">
          <!-- <div class="progress"></div>
          <div class="name">Run</div>
          <div class="sunday">{{dayName1}} {{dayDate1}}</div>
          <div class="monday">Mon</div>
          <div class="tuesday">Tue</div>
          <div class="wednesday">Wed</div>
          <div class="thursday">Thu</div> -->
          <div class="d-flex stats-container">

          </div>
          <div v-for="slot in weekdaySlots" :key="slot.dayName" class="day-label">
            <p>{{slot.dayName}}</p>
            <p>{{slot.dateName}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>

</template>
<script>
import dayjs from 'dayjs'
export default {

computed: {

  weekdaySlots() {
    return [
      {dayName: dayjs().format('ddd'), dateName: dayjs().format('DD')},
      {dayName: dayjs().add(1, 'day').format('ddd'), dateName: dayjs().add(1, 'day').format('DD')},
      {dayName: dayjs().add(2, 'day').format('ddd'), dateName: dayjs().add(2, 'day').format('DD')},
      {dayName: dayjs().add(3, 'day').format('ddd'), dateName: dayjs().add(3, 'day').format('DD')},
      {dayName: dayjs().add(4, 'day').format('ddd'), dateName: dayjs().add(4, 'day').format('DD')},
    ]
  }
}

}
</script>