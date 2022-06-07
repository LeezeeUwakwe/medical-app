<template>
  <div class="container">
    <h1 class="cases">Reported Cases</h1>
    <bar-chart :data="barChartData" :options="barChartOptions" :height="110" />
  </div>
</template>

<script>

const chartColors = {
  ash: 'rgb(158,177,184)',
  gray: 'rgb(122,122,122)'
};

export default {
  data() {
    return {
      barChartData: {
        labels: ['Tuberclosis', 'Malaria', 'Typhoid', 'HIV', 'Scurvy', 'Covid-19', 'Pregnancy', 'Pnuemonia', 'Common cold',
        'Influenza', 'Colon cancer', 'Diabetes'],
        datasets: [
          {
            label: 'Cases',
            backgroundColor: chartColors.ash,
            data: [100, 150, 200, 225, 140, 145, 225, 110, 130, 125, 150, 50,],
            borderWidth: 1,
            borderSkipped: false,
            borderRadius: '10px',
            fontColor: chartColors.gray,
          }

        ]
      },
      barChartOptions: {
        responsive: true,
        legend: {
          display: false,
        },
        scales: {
          xAxes: [
            {
              gridLines: {
                display: false,
              },
               ticks: {
               fontSize: 11,
               fontColor: '#7A7A7A',
               fontWeight: 400
               
              },
               barPercentage: 0.08,
            },
          ],
          yAxes: [
            {
                  gridLines: {
                    display: true,
                    borderDash: [4, 4],
                    color: '#E4EAEA',
                    drawBorder: false,
                  },
              ticks: {
               beginAtZero: true,
               fontSize: 10,
               fontColor: '#7A7A7A',
               fontWeight: 400


               
              },
              steps: 10,
              stepValue: 5,
              max: 250,

            }
          ]
        }
      }
    }
  },
 
}
</script>

<style lang="scss" scoped> 
.cases {
  color: #3D3D3D;
  font-size: 14px;
  font-weight: 600;
  margin: 5px 0 2.5rem 0;
}


 
</style>
