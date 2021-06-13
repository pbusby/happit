<template>
  <div class="home">
    <weekday-nav />
    <habit/>
    <habit/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Habit from '@/components/Habit.vue'
import WeekdayNav from '@/components/WeekdayNav.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,
    Habit,
    WeekdayNav
  }
}
</script>
