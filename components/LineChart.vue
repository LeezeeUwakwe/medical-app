<template>
  <div>
   <chartjs-line
   :beginzero="beginZero" :datalabel="datalabel" :labels="labels" :data="data" :second-data="secondData" :fill="fill" 
   :backgroundcolor="bgColor" :bordercolor="borderColor" :borderwidth="borderWidth"
 />
  
  </div>
</template>

<script>
  export default {
    data () {
      return {
        beginZero: true,
        labels : ["JAN","FEB","MAR","APR","MAY","JUN","JUL","AUG","SEP","OCT","NOV","DEC"],
        data: [0, 300, 300, 350, 400, 225, 400, 200, 100, 300, 200, 400, 500],
        fill: true,
        bgColor: '#F6F8F8',
        borderColor: '#799794',
        borderWidth: '1px',

      }
    }
    
  }
</script>

<style lang="scss" scoped>
body {
    font-family: "Avenir LT Std";
}

</style>