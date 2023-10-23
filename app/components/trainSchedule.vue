<template>
    <div>
        {{schedule}}
        <dynamicInput inputType="number" v-model="schedule.sn" />
        <dynamicInput inputType="number" v-model="schedule.trainNo" />
        <dynamicInput inputType="text"   v-model="schedule.stationCode" />
        <dynamicInput inputType="number" v-model="schedule.a1" />
        <dynamicInput inputType="number" v-model="schedule.a2" />
        <dynamicInput inputType="number" v-model="schedule.a3" />
        <dynamicInput inputType="number" v-model="schedule.sl" />
        <dynamicInput inputType="text"   v-model="schedule.stationName" />
        <dynamicInput inputType="number" v-model="schedule.routeNumber" />
        <dynamicInput inputType="text" v-model="schedule.arrivalTime" />
        <dynamicInput inputType="text" v-model="schedule.departureTime" />
        <dynamicInput inputType="number" v-model="schedule.distance" />
        
    </div>
</template>
 
 
<script setup>
 
 const schedule = reactive({
        sn: 1,
        trainNo: 107,
        stationCode: "SWV",
        a1: 100,
        a2: 100,
        a3: 100,
        sl: 100,
        stationName: "SAWANTWADI R",
        routeNumber: 1,
        arrivalTime: "00:00:00",
        departureTime: "10:25:00",
        distance: 0,
        id: 1
 })

</script>
 
