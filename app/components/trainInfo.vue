<template>
    <div class="row justify-content-center">
        <div class="col-9">
            <div class="row justify-content-center mt-3">
                <div class="col-11">
                    <h2>Train Info</h2>
                </div>
            </div>
            <div class="row mt-4 justify-content-around">
                <div class="col-3">
                    <dynamicInput inputType="number" labelName="trainNo" inputName="Train No" v-model="info.trainNo"  />
                </div>
                <div class="col-3">
                    <dynamicInput inputType="text" labelname="trainName" inputName="Train Name"  v-model="info.trainName" />
                </div>
                <div class="col-3">
                    <dynamicInput inputType="text" labelName="days" inputName="Days" v-model="info.days" />
                </div>
            </div>
            <div class="row mt-4 justify-content-around">
                <div class="col-3">
                    <dynamicInput inputType="text" labelName="destinationStationName" inputName="Destination station Name" v-model="info.destinationStationName" />
                </div>
                <div class="col-3"></div>
                <div class="col-3">
                    <dynamicInput inputType="text" labelName="sourceStationName" inputName="Source station Name" v-model="info.sourceStationName" />
                </div>
            </div>
        </div>
    </div>
</template>


<script setup>

 const info = reactive({
    trainNo: 107,
    trainName: "SWV-MAO-VLNK",
    sourceStationName: "SAWANTWADI ROAD",
    destinationStationName: "MADGOAN JN.",
    days: "Saturday",
    id: 1
 })

</script>

