 <template>
    <client-only>
        <line-chart
        :data="chartData" 
        :chart-options="options"
        :height="42"
        :width="100">
        </line-chart>
    </client-only>
  </template>

  <script>
  export default {
    data() {
      return {
        chartData: {
           labels: ['Jan', 'Feb', 'Mar', 'Apr', 'may', 'Jun', 'Jul', 'Aug', 'Sep',
        'Oct', 'Nov', 'Dec'],
          datasets: [
          {
            label: 'New Patients',
            data: [400, 200, 28, 35, 12,400, 200, 28, 35, 12,10,10,500],
             color: '#799794',
             backgroundColor: '#F0F3F3',
             borderColor: '#799794',

          },
          {
            label: 'Returning Patients',
            data: [100, 300, 200, 100, 200,100,300,200,400,100,200,300,500],
            backgroundColor: '#FBFCFC',
            borderColor: '#CDB1A8',

          }
          ]
        },

        options: {

        // responsive: true,
        // legend: {
        //   display: false,
        // },
        scales: {
          // x: [
          //   {
          //     gridLines: {
          //       display: false,
          //     },
          //      ticks: {
          //       display: false,

          //      fontSize: 11,
          //      fontColor: '#7A7A7A',
          //      fontWeight: 400
               
          //     },
          //   },
          // ],
       y: {
            max: 500,
            min: 0,
            ticks: {
                stepSize: 100
            }
        }
        }


        }
      };
    }
  }
  </script>

  <style lang="scss" scoped>
  #line-chart {
    height: 100px !important;
  }
  </style>