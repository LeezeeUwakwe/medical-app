<template>
  <div>
    <Navbar />
    <!-- <NavBBar /> -->
    <div class="container">
    <div class="finance-header">
    <h1 class="finance-title">Patients Report</h1>
     
    <div class="finance-content space-x-7">
       <Search
          :search="search" 
          class="mt-1"
          placeholder="Search"
        />      
        <Today-btn />
    </div>
   </div>

   <div class="card-container">
     <Card :cards="cards" />
   </div>

     
       <div class="mt-6">
        <h2 class="patient-list">Patients List</h2>
         <FinanceTable />
      </div>

       <div class="navigator-wrapper">
            <div class="navigator">
           <img src="~/assets/images/right-arrow.png" class="right-arrow rounded-full" alt="">
           <p class="navigator-text"><span>10</span> of <span>10,000</span> </p>
           <img src="~/assets/images/left-arrow.png" class="left-arrow rounded-full" alt="">
         </div>
        </div>









    </div>
  </div>
</template>

<script>
  export default {
    data() {
        return {
        cards: [
          
         {
          icon: "/icon.png",
          title: "Patients Today",
          numbers:"10,000",
          subIcon: "",
          subText: "",
          subColor: ""
        },
         {
          icon: "/icon.png",
          title: "New Patients",
          numbers:"10,000",
          subIcon: "",
          subText: "",
          subColor: ""
        },
            ]
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
.card-container {
  width: 39%;
}

.finance-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 5.5rem;
}
.finance-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.finance-title {
  color: #292929;
  font-size: 25px;
  font-weight: 600;
}
.patient-list {
  font-size: 14px;
  color: #292929;
  font-weight: 600;
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







</style>