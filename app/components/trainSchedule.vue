<template>
        <div class="row mt-3 mb-3 justify-content-center">
            <div class="col-9">
                <div class="row justify-content-center mt-3">
                    <div class="col-11">
                        <h2>Train Schedule</h2>
                    </div>
                </div>
                <div class="row mt-4  justify-content-around">
                    <div class="col-2">
                        <dynamicInput inputType="number" labelName="sn" inputName="SN" v-model="schedule.sn" />
                    </div>
                    <div class="col-2">
                        <dynamicInput inputType="text" labelName="stationCode" inputName="Station Code"  v-model="schedule.stationCode" />
                    </div>
                    <div class="col-2">
                        <dynamicInput inputType="text" labelName="stationName" inputName="Station Name" v-model="schedule.stationName" />
                    </div>
                    <div class="col-2">
                        <dynamicInput inputType="number" labelName="routeNumber" inputName="Route Number" v-model="schedule.routeNumber" />
                    </div>
                </div>
                <div class="row mt-4  justify-content-around">
                    <div class="col-2">
                        <dynamicInput inputType="number" labelName="a1" inputName="1A" v-model="schedule.a1" />
                    </div>
                    <div class="col-2">
                        <dynamicInput inputType="number" labelName="a2" inputName="2A" v-model="schedule.a2" />
                    </div>
                    <div class="col-2">
                        <dynamicInput inputType="number" labelName="a3" inputName="3A" v-model="schedule.a3" />
                    </div>
                    <div class="col-2">
                        <dynamicInput inputType="number" labelName="sl" inputName="SL" v-model="schedule.sl" />
                    </div>
                </div>
                <div class="row mt-4  justify-content-around">
                    <div class="col-3">
                        <dynamicInput inputType="time" labelName="arrivalTime" inputName="Arrival Time" v-model="schedule.arrivalTime" />
                    </div>
                    <div class="col-3">
                        <dynamicInput inputType="time" labelName="departureTime" inputName="Departure Time" v-model="schedule.departureTime" />
                    </div>
                    <div class="col-3">
                        <dynamicInput inputType="number" labelName="distance" inputName="Distance" v-model="schedule.distance" />
                    </div>
                </div>
            </div>
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

