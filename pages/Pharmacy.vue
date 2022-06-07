<template>
  <div>
    <!-- <NavBBar /> -->
    <Navbar />
    <div class="container">

    <div class="pharmacy-header">
    <h1 class="pharmacy-title">Pharmacy</h1>
    <div class="pharmacy-content space-x-7">
       <Search
          :search="search" 
          class="mt-1"
          placeholder="Search"
        />      
        <Today-btn />
       <nuxt-link to="NewMedication" class="new-medication">New Medication</nuxt-link>

    </div>
   </div>
    <div class="card-container"> 
     <Card :cards="cards" />
   </div>
    

      <div class="mt-6">
        <h2 class="medications">Medications</h2>
         <PharmacyTable />
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
          icon: "/medicine.png",
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
.pharmacy-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 5.5rem;
}
.pharmacy-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.pharmacy-title {
  color: #292929;
  font-size: 25px;
  font-weight: 600;
}
.card-container {
  width: 39%;
}

.new-medication {
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
a {
  text-decoration: none;
}
.medications{
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