<template>
  <v-card>

    <v-tabs
      v-model="tab"
      grow
    >
      <v-tab
        v-for="item in items"
        :key="item"
        class="tracking-normal"
      >
        {{ item }}
      </v-tab>
    </v-tabs>
  <!-- Bio Data -->
    <v-tabs-items v-model="tab">
      <v-tab-item class="">
        <v-card
          flat
          class=""
          >
          <div class="base-wrapper mt-7">
         <div class="activities">
           <div class="chart-wrapper">
            <div class="line-chart">
              <h1 class="chart-title">Pateints</h1>
            <LineChart />
          </div>

        <div class="doughChart-wrapper">
          <h1 class="chart-title">Gender</h1>
      <DoughnutChart />
        </div>
           </div>
           
        
      </div>          
      </div>

          <div class="chart mt-8">
           <Chart />
          </div>

          <div class="linear-wrapper mt-8">
            <h1 class="linear-title">HMOs And Patients Covered</h1>
           
            <ProgressBar />
          </div>
         
          
           

        </v-card>
      </v-tab-item>



      <!-- Medical History -->
       <v-tab-item>
        <v-card
          flat
          light
        >
        <MedicalHistory />
        </v-card>
      </v-tab-item>


      <!-- HMO -->
       <v-tab-item>
        <v-card
          flat
        >
           <div class="hmo-heading px-4 bg-white mt-6">
           <div class="update space-x-1">
             <img src="~/assets/images/update.png" class="w-5 h-5" alt="">
             <p class="update-text">Update</p>
           </div>

           <div class="hmo-wrapper space-x-40 bg-white">
              <div>
                <h2 class="hmo-title">HMO Name</h2>
                <p class="hmo-text">Reliance HMO</p>
              </div>
              <div>
                <h2 class="hmo-title">HMO Type</h2>
                <p class="hmo-text">Private</p>
              </div>
            </div> 

            <div class="py-4">
              <h2 class="hmo-title">HMO Teir</h2>
              <p class="hmo-text">Premium Individual</p>
            </div>  
           </div>  

           <div class=" bg-white">
             <h2 class="pl-4 hmo-title bg-white">Tier Benefits </h2>
             
              <ul
                class="list-wrapper">
                <li
                  v-for="benefit in benefits"
                  :key="benefit"
                  class="item pt-5 ml-7">{{benefit.listItem}}
                </li>
                </ul>
             </div>
             </v-card>
      </v-tab-item>

      <!-- Finance -->
       <v-tab-item>
        <v-card
          flat
        >
        <div class="finance-wrapper">
          <div class="finance space-x-6">
        <Card
         :cards="cards" 
        class="w-9/12"/>
        <nuxt-link to="#" class="gen-receipt">Generate Receipt</nuxt-link>
        </div>
        <h1 class="receipt-history mt-4">Receipt History</h1>
        </div>
        
        </v-card>
      </v-tab-item>



      <!-- Consultation -->
        <v-tab-item>
        <v-card
          flat
        >
        <div class="consultation">
          <div class="consultation-wrapper">
            <button class="new-consultation mt-6" @click="consult = !consult">{{ consult ? 'New' : 'End'  }} Consultation</button>
          </div>
          <Consulation v-if="consult" />
          <NewConsultation v-else />
          <!-- <div v-else></div> -->
        </div>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>

<script>

  export default {
    data() {
        return {
            consult: true,
            power: 40,
            email: "",
            tab: null,
            items: [
                "Patient Analytics",
                "Staff Analytics",
                "Financial Analytics",
                "Pharmacy Analytics",
                "Lab Analytics",
            ],
            // text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
            benefits: [
                {
                    listItem: "Primary/Secondary Dental Care",
                },
                {
                    listItem: "Out Patient Care, General and Specialist Consultation",
                },
                {
                    listItem: "Minor, Intermediate, Major Surgeries and Procedures",
                },
                {
                    listItem: "Admissions (Including Feeding)",
                },
                {
                    listItem: "Evacuation (Home/Hospital to Hospital & Road Side to Hospital)",
                },
                {
                    listItem: "X-Rays, Laboratory & Diagnostic Tests",
                },
                {
                    listItem: "Physiotherapy Sessions (Up to Approved Limits)",
                },
                {
                    listItem: "NPI Immunizations",
                },
                {
                    listItem: "Antenatal care, Induction of labour & Normal delivery",
                },
                {
                    listItem: "Assisted delivery & Emergency or Medically indicated Elective Caesarean Section",
                },
                {
                    listItem: "HIV/AIDS – to the Extent of Diagnosis + Treatment at Free Specialist Centres",
                },
                {
                    listItem: "Psychiatry Cover up to 8 Weeks",
                },
                {
                    listItem: "Advanced and Complex Investigations (Including CT Scan, MRI Scan)",
                },
                {
                    listItem: "Treatment of ENT diseases and removal of foreign bodies",
                },
                {
                    listItem: "ENT Surgeries",
                },
            ],
            cards: [
                {
                    icon: "/bed-frame.png",
                    title: "Total Due",
                    numbers: "1,000,000",
                },
                {
                    icon: "/bed-frame.png",
                    title: "Total Paid",
                    numbers: "1,000,000",
                },
                {
                    icon: "/bed-frame.png",
                    title: "Pending Payment",
                    numbers: "1,000,000",
                },
                {
                    icon: "/bed-frame.png",
                    title: "Covered by HMO",
                    numbers: "1,000,000",
                },
            ],
        };
    },
}
</script>

<style lang="scss" scoped>

.v-tab::v-deep {
  text-transform: none;
  color: #7a7a7a;
  font-size: 13px;
  font-weight: 400;
  letter-spacing: 0;
}
.v-tabs-slider {
    background-color: #283231 !important;
    width: 20%;
    margin-left: 15%;
    height: 4px
}

.theme--light.v-tabs > .v-tabs-bar .v-tab:not(.v-tab--active) {
  margin-left: -14px;
  padding-right: 85px;
}
.v-tab--active {
  color: #283231 !important;
  font-weight: 600;
  margin-left: -14px;
  padding-right: 85px;
  background-color: #FAFAFA;
}

.v-tabs--grow > .v-tabs-bar .v-tab {
  flex: none;
}

.update {
  display: flex;
  justify-content: end;
  align-items: center;
  padding: 10px 20px;
}
.update-text {
  color: #799794;
  font-size: 400;
  font-size: 14px;
}
.hmo-title {
  font-size: 10px;
  color: #7A7A7A;
  font-weight: 400;
}
.hmo-text {
  font-size: 15px;
  color: #292929;
 }
.hmo-wrapper {
  display: flex;
  align-items: center;
}
.v-sheet.v-card:not(.v-sheet--outlined) {
  box-shadow: none;
  border: 1px solid #FAFAFA;

  // background-color: #FAFAFA;
}

.theme--light.v-tabs::v-deep > .v-tabs-bar {
  background-color: #FAFAFA;
  border-bottom: 1px solid #E0E0E0;


}
.list-wrapper {
  display: flex;
  // justify-content: space-between;
  flex-wrap: wrap;
  // width: 90%;
  margin: 0 auto;
  background-color: white ;
  }
.item  {
  width: 24%;
  font-size: 13px;
  list-style: disc;
  width: 210px;
  color: #3D4C4A;
  font-weight: 600;
}
.consultation-wrapper,
.staff-wrapper {
  display: flex;
  justify-content: end;
  background-color: #FAFAFA;
  margin-bottom: 30px;
}
.new-consultation,
.new-staff {
  background-color: #799794 ;
  width: 12rem;
  border-radius: 4px;
  font-size: 14px;
  font-weight: 400;
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px 0;
} 

// .v-card > *:last-child:not(.v-btn):not(.v-chip):not(.v-avatar) {
//   background-color: #FAFAFA;
//   padding: 0 0 20px 0;
// }
.v-expansion-panel-content__wrap {
  border-top: 10px solid red;
}

.v-sheet.v-card[data-v-a04987ec]:not(.v-sheet--outlined) {
    background-color: #FAFAFA;
}
.input-field {
  width: 42%;
}
.activities {
  margin-top: 30px
}
.activities-title,
.patient-queued {
   font-size: 15px;
   color: #292929;
}
.api {
  width: 100%;
  margin-top: 6px;
}
.api img {
  max-width: 100%;
}
// .base-wrapper {
//   display: flex;
//   flex-wrap: wrap;
//   justify-content: space-between;
//   padding: 20px 70px;
//   background-color: #fff;
//   margin-top: 25px;
//   border: 1px solid #E0E0E0;
//   border-radius: 4px;
// }
.finance {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.gen-receipt {
  background-color: #799794 ;
  width: 12rem;
  border-radius: 4px;
  font-size: 14px;
  font-weight: 400;
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px 0;
  align-self: flex-end;
}
.receipt-history {
  font-size: 12px;
  color: #292929;
  font-weight: 600;
}
.v-sheet.v-card[data-v-72d294ec]:not(.v-sheet--outlined) {
  background-color: #FAFAFA;
}
.chart {
  background-color: #ffff;
  border: 1px solid #E0E0E0;
  border-radius: 4px;
}
.linear-wrapper {
  width: 50%;
  background-color: #fff;
  border: 1px solid #E0E0E0;
  border-radius: 5px;
  padding: 12px 12px;
}
.linear-title {
  font-size: 14px;
  color: #3D3D3D;
  font-weight: 600;
}
.chart-wrapper {
  background-color: #fff;
  border: 1px solid #E0E0E0;
  border-radius: 5px;
  padding: 10px 15px;
  display: flex;
  justify-content: space-between;
}


.line-chart {
  width: 70%;
  // height: 300px;
}
.chart-title {
  font-size: 14px;
  color: #3D3D3D;
  font-weight: 600;
}
.doughChart-wrapper {
   width: 28%;
}
.v-application p {
  margin-bottom: 0;
}
a {
  text-decoration: none;
}


</style>