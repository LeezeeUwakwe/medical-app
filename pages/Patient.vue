<template>
  <div>
   <Navbar />
   <!-- <NavBBar /> -->
   <div class="container">

   <div class="patient-header">
    <h1 class="patient-title">Patients</h1>
     
    <div class="header-content">
       <Search
          :search="search" 
          class="mt-1"
          placeholder="Search"
        />      
        <Today-btn />
      <nuxt-link to="NewPatient" class="new-patient">New Patient</nuxt-link>
    </div>
   </div>
      
        <Card
      :cards="cards" />

      

      <div class="mt-6">
        <h2 class="patient-list">Patients List</h2>
         <PatientTable />
        <div class="navigator-wrapper">
            <div class="navigator">
           <img src="~/assets/images/right-arrow.png" class="right-arrow rounded-full" alt="">
           <p class="navigator-text"><span>10</span> of <span>10,000</span> </p>
           <img src="~/assets/images/left-arrow.png" class="left-arrow rounded-full" alt="">
         </div>
        </div>
        


      </div>





   </div>
  </div>
</template>

<script>
  export default {
    data() {
        return {
            search: "Search",
            cards: [
                {
                    icon: "/bed-frame.png",
                    title: "Total Patients",
                    numbers: "10,000",
                    subIcon: "/success-arrow.png",
                    subText: "15% today",
                    subColor: "success"
                },
                {
                    icon: "/bed-frame.png",
                    title: "Patients Today",
                    numbers: "10,000",
                    subIcon: "/error-arrow.png",
                    subText: "15% today",
                    subColor: "warning"
                },
                {
                    icon: "/bed-frame.png",
                    title: "Patient Admitted",
                    numbers: "10,000",
                    subIcon: "/success-arrow.png",
                    subText: "15% today",
                    subColor: "success"
                },
                {
                    icon: "/bed-frame.png",
                    title: "Patients with HMO",
                    numbers: "1,000,000",
                    subIcon: "/success-arrow.png",
                    subText: "15% today",
                    subColor: "success"
                },
                {
                    icon: "/bed-frame.png",
                    title: "Pending Settlement",
                    numbers: "N10m",
                    subIcon: "/success-arrow.png",
                    subText: "15% today",
                    subColor: "success"
                },
            ],
        };
    },
}
</script>

<style lang="scss" scoped>
.container {
   padding: 2rem;
   margin: 0 auto; 
   margin-bottom: 4rem;
}
.patient-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 5.5rem; 
  
}
.header-content {
  display: flex;
  align-items: center;
  margin-left: 10px;
}

.patient-title {
  color: #292929;
  font-size: 25px;
  font-weight: 600;
}
.patient-list {
  font-size: 14px;
  color: #292929;
  font-weight: 600;
}
.new-patient {
  background-color: #799794 ;
  width: 12rem;
  border-radius: 6px;
  font-size: 14px;
  font-weight: 400;
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px 0;
  margin-left: 20px;
}
.navigator-wrapper {
  display: flex;
  justify-content: flex-end;
}
.navigator {
  display: flex;
  justify-content: space-between;
  margin: 20px 0;
  align-items: center;
  width: 140px;
}
.navigator-text {
  color: #3D3D3D;
  font-size: 11px;
}
.right-arrow,
.left-arrow {
  background-color: #D2DCDB;
  width: 25px;
  height: 25px;
  border-radius: 50%;
}
.v-application p {
  margin-bottom: 0;
}

a {
  text-decoration: none;
}



</style>