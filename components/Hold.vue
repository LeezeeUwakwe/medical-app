  <template>
    <client-only>
        <line-chart :data="chartData" :options="chartOptions"></line-chart>
    </client-only>
  </template>
    <chartjs-line
   :beginzero="beginZero" :datalabel="datalabel" :labels="labels" :data="data" :fill="fill" 
   :backgroundcolor="bgColor" :bordercolor="borderColor" :options="options" :chart-data="datacollection"
 />

<script>
export default { 
  data() {
    return {
      chartData: {
        labels: [
          "week 1",
          "week 2",
          "week 3",
          "week 4",
          "week 5",
          "week 6",
          "week 7",
          "week 8",
          "week 9",
          "week 10",
        ],
        datasets: [
          {
            data: [86, 114, 106, 106, 107, 111, 133, 221, 783, 2478],
            label: "Africa",
            borderColor: "#3e95cd",
            fill: false,
          },
          {
            data: [282, 350, 411, 502, 635, 809, 947, 1402, 3700, 5267],
            label: "Asia",
            borderColor: "#8e5ea2",
            fill: false,
          },
          {
            data: [168, 170, 178, 190, 203, 276, 408, 547, 675, 734],
            label: "Europe",
            borderColor: "#3cba9f",
            fill: false,
          },
          {
            data: [40, 20, 10, 16, 24, 38, 74, 167, 508, 784],
            label: "Latin America",
            borderColor: "#e8c3b9",
            fill: false,
          },
          {
            data: [6, 3, 2, 2, 7, 26, 82, 172, 312, 433],
            label: "North America",
            borderColor: "#c45850",
            fill: false,
          },
        ],
      },
      
      chartOptions: {
        responsive: true,
        legend: {
          display: false,
        },
        tooltips: {
          titleFontSize: 20,
          bodyFontSize: 25,
        },
        scales: {
          xAxes: [],
          yAxes: [
            {
              ticks: {
                beginAtZero: true,
              },
            },
          ],
        },
      },
    };
  },
};
</script>


<template>
  <div>
   <chartjs-line
   :beginzero="beginZero" :datalabel="datalabel" :labels="labels" :data="data" :fill="fill" 
   :backgroundcolor="bgColor" :bordercolor="borderColor" :options="options"
 />
  </div>
</template>

<script>
  export default {
    data () {
      return {
        beginZero: true,
        datalabel: 'New patients',
        labels : ["JAN", "FEB","MAR","APR","MAY","JUN","JULY","JUL","AUG","SEP","OCT","NOV","DEC"],
        data: [0, 100, 200, 300, 400, 500],
        fill: true,
        bgColor: '#F1F4F3',
        borderColor: '#799794',
  

      }
    }
    
  }
</script>