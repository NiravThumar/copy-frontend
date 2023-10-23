<template>
    <div class="container">
        <div class="row">
            <fieldset class="form-group boredr">
                <legend>Train Info</legend>
                <div class="col-12">
                    <div class="row mt-2 mb-3">
                        <div class="col-4">
                            <dynamicInput inputType="number" labelName="trainNo" inputName="Train No" v-model="info.trainNo"  />
                        </div>
                        <div class="col-4">
                            <dynamicInput inputType="text" labelname="trainName" inputName="Train Name"  v-model="info.trainName" />
                        </div>
                        <div class="col-4">
                            <dynamicInput inputType="text" labelName="days" inputName="Days" v-model="info.days" />
                        </div>
                    </div>
                    <div class="row justify-content-between">
                        <div class="col-5">
                            <dynamicInput inputType="text" labelName="destinationStationName" inputName="Destination station Name" v-model="info.destinationStationName" />
                        </div>
                        <div class="col-5">
                            <dynamicInput inputType="text" labelName="sourceStationName" inputName="Source station Name" v-model="info.sourceStationName" />
                        </div>
                    </div>
                </div>
            </fieldset>
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

