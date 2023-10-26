<template>
  <div class="container shadow-lg mt-3">

    <!-- Train Info heading -->
    <div class="row pt-3 pb-3">
      <div class="col-10">
        <h3>Train Info</h3>
      </div>
      <div class="col-1">
        <button class="btn btn-success">Update</button>
      </div>
      <div class="col-1">
        <button class="btn btn-danger">Delete</button>
      </div>
    </div>
    <!-- {{trainInfo}} -->
    {{ trainSchedule }}
    <!-- train info details -->
    <div class="row justify-content-between">
        <div class="col-3">
          <span class="color-blue fs-5">Train No  : </span>
           <span class="train-color fs-5">{{trainInfo.trainNo}}</span>
        </div>
        <div class="col-3">
          <span class="color-blue fs-5">Train Name  : </span>
           <span class="train-color fs-5">{{trainInfo.trainName }}</span>
        </div>
        <div class="col-3">
          <span class="color-blue fs-5">Days : </span>
           <span class="train-color fs-5">{{ trainInfo.days }}</span>
        </div>
    </div>
    <div class="row justify-content-between">
      <div class="col-4">
        <span class="color-blue fs-5">Source : </span>
          <span class="train-color fs-5">{{trainInfo.sourceStationName}}</span>
      </div>
      <div class="col-4">
        <span class="color-blue fs-5">Destination : </span>
          <span class="train-color fs-5">{{trainInfo.destinationStationName}}</span>
      </div>
    </div>

    <!-- <div class="row pt-5 pb-3">
      <div class="col-11">
        <h3>Train Schedule</h3>
      </div>
      <div class="col-1">
        <button class="btn btn-primary">Add</button>
      </div>
    </div>
    <div class="row justify-content-between">
      <div class="col-3">
        <span class="color-blue fs-5">SN : </span>
          <span class="train-color fs-5">{{trainSchedule[0].sn}}</span>
      </div>
      <div class="col-3">
        <span class="color-blue fs-5">Station Code : </span>
          <span class="train-color fs-5">{{trainSchedule[0].stationCode}}</span>
      </div>
      <div class="col-3">
        <span class="color-blue fs-5">Station Name : </span>
          <span class="train-color fs-5">{{trainSchedule[0].stationName}}</span>
      </div>
      <div class="col-3">
        <span class="color-blue fs-5">Route Number : </span>
          <span class="train-color fs-5">{{ trainSchedule[0].routeNumber }}</span>
      </div>
    </div> -->



  </div>
</template>

<script setup>
let route = useRoute()
let trainNo = route.params.trainNo;

let trainInfoUrl = computed(() => {
  return `http://localhost:3006/trainInfo?trainNo=${trainNo}`
})
let trainScheduleUrl = computed(() => {
  return `http://localhost:3006/trainSchedule?trainNo=74641`
})

let { data , pending1, error1, refresh1 } = await useFetch(trainInfoUrl, {
  watch: [trainInfoUrl]
});
let { 0: trainInfo} = data.value;

let { data: trainSchedule, pending2, error2, refresh2 } = await useFetch(trainScheduleUrl, {
  watch: [trainScheduleUrl]
})

console.log(trainSchedule)

</script>

<style scoped>
  .color-blue {
    color: #0404e7fd;
  }

  .train-color {
    color: #8b8d90;
  }
</style>

