<template>
  <div>
    <!-- <NavBBar /> -->
    <Navbar />
    <div class="container">
       <div class="staff-header">
    <h1 class="staff-title">Staff</h1>
     
    <div class="staff-content">
       <Search
          :search="search" 
          class="mt-1"
          placeholder="Search"
        />      
        <Today-btn />
       <nuxt-link to="NewStaff" class="new-staff">New Staff</nuxt-link>
   
    </div>
   </div>

     <div>
       <Card :cards="cards" />
      </div>

      <div class="staff-table">
        <h2 class="staff-list mt-6">Staff List</h2>
        <StaffTable />

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
                    icon: "/user.png",
                    title: "Total Staff",
                    numbers: "10,000",
                },
                {
                    icon: "/user.png",
                    title: "Nurses on Duty",
                    numbers: "10,000",
                },
                {
                    icon: "/user.png",
                    title: "Doctors on Duty",
                    numbers: "10,000",
                },
                {
                    icon: "/user.png",
                    title: "Active Staff",
                    numbers: "10,000",
                    subText: "15% of staffs",
                    subColor: "success"
                },
                {
                    icon: "/user.png",
                    title: "Inactive Staff",
                    numbers: "10,000",
                    subText: "15% of staffs",
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
.staff-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 5.5rem;
}
.staff-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.staff-title {
  color: #292929;
  font-size: 25px;
  font-weight: 600;
}
.new-staff {
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
.staff-list {
  font-size: 14px;
   color: #292929;
   font-weight: 600;
}
.v-application p {
  margin-bottom: 0;
}
a {
  text-decoration: none;
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
</style>