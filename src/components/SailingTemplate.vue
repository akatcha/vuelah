<template>
  <div class="action-item">
    <div class="action-title">
      <h4>Beulah Sailing</h4>
    </div>
    <a class="page-link" href="https://www.lbyc.us/">LBYC Home Page</a>
    <b-container>
      <h6 class="calendar-title">Calendar</h6>
      <div class="small">
        <Calendar></Calendar>
      </div>
    </b-container>
  </div>
</template>

<script>
import Calendar from "./Calendar";
export default {
  components: { Calendar }
};
</script>
<style scoped>
.action-title {
  margin: 20px;
}

.calendar-title {
  margin-bottom: -3rem;
  margin-top: 1rem;
}

.action-item {
  /* height: 50rem; */
  max-height: 65vh;
  overflow-y: auto;
}

.page-link {
}

.small {
  transform: scale(0.8, 0.8);
  -ms-transform: scale(0.8, 0.8); /* IE 9 */
  -webkit-transform: scale(0.8, 0.8); /* Safari and Chrome */
  -o-transform: scale(0.8, 0.8); /* Opera */
  -moz-transform: scale(0.8, 0.8); /* Firefox */
}
</style>
