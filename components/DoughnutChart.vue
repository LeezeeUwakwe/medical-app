<template>
  <div>
    <chartjs-doughnut :labels="labels" :dataset="datasets" :option="option" />

  </div>
</template>

<script>
  export default {
    data () {
      return {
        labels: ['Female', 'Male'],
        datasets: [
           {
           data: ['6,000,000', '4,000,000'],
           backgroundColor: ['Red', 'Yellow'],
          }
        ],
        option: {
          title: {
            display: true,
            text: 'Gender'
          }
        }
      }
    }
    
  }
</script>

<style lang="scss" scoped>

</style>