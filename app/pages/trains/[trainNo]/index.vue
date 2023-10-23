<template>
    <div>
          <!-- <div v-if="trainInfoData"> -->
            {{trainInfoData}}
          <!-- </div> -->
          <!-- <div v-if="trainScheduleData"> -->
            {{trainScheduleData}}
          <!-- </div> -->
    </div>
</template>

<script setup>
    let route = useRoute()
    let trainNo = route.params.trainNo;

    let trainInfoUrl = computed(()=>{
            return `http://localhost:3002/trainInfo?trainNo=${trainNo}`
    }) 
    let trainScheduleUrl =  computed(()=>{
            return `http://localhost:3002/trainSchedule?trainNo${trainNo}`
    }) 

    let {trainInfoData,pending1,error1,refresh1} = await useAsyncData(()=>{
        console.log('trainInfo:',trainInfoUrl)
        $fetch(trainInfoUrl,{
        watch:[trainInfoUrl]
     })
    })
    let {trainScheduleData,pending2,error2,refresh2} =await  useAsyncData(()=>$fetch(trainScheduleUrl,{
        watch:[trainScheduleUrl]
    }))

</script>

