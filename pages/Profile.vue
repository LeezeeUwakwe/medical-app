<template>
  <div>
    <Navbar />
    <!-- <NavBBar /> -->
    <div class="container">

       <nuxt-link 
      :src="image" 
      tag="img" 
      to="/NewStaff"
      class="mt-10 w-7 h-7">
    </nuxt-link>

    <div class="profile-container">

    <div class="profile-wrapper">
     <div class="profile-content">

       <div class="right">
         <div class="detail-wrapper">
         <h2 class="detail-title">Position</h2>
         <p class="detail-info">Doctor</p>
         </div>
         <div class="detail-wrapper">
         <h2 class="detail-title">First Name</h2>
         <p class="detail-info">Oluwatobiloba</p>
         </div>
         <div class="detail-wrapper">
         <h2 class="detail-title">Last Name</h2>
         <p class="detail-info">Afolabi</p>
         </div>
         <div class="detail-wrapper">
         <h2 class="detail-title">Gender</h2>
         <p class="detail-info">Male</p>
         </div>

         <div class="detail-wrapper">
         <h2 class="detail-title">Email Address</h2>
         <p class="detail-info">afolabitobi200.gmail.com</p>
         </div>

         <div class="detail-wrapper">
         <h2 class="detail-title">Phone Number</h2>
         <p class="detail-info">08138814501</p>
         </div>
        
       </div>



       <div class="left">
           <div class="detail-wrapper">
         <h2 class="detail-title">Residential Address</h2>
         <p class="detail-info">04 Barnawa Close, Barnawa Kaduna</p>
         </div>
           <div class="detail-wrapper">
         <h2 class="detail-title">I.D Number</h2>
         <p class="detail-info">142314</p>
         </div>
           <div class="detail-wrapper">
         <h2 class="detail-title">Patients Attendeed to</h2>
         <p class="detail-info">142</p>
         </div>
           <div class="detail-wrapper">
         <h2 class="detail-title">Year Employed</h2>
         <p class="detail-info">27-12-2022</p>
         </div>


       </div>

       
     </div>
    
      <div class="mt-4">
        <div class="profile-photo">
          <img src="~/assets/images/unsplash_279xIHymPYY.png" alt="">
      </div>
      <div class="active px-3 py-2 mt-4">
        <p class="text-sm">Active</p>
      </div>
      </div> 
    </div>

    

   <div class="edit space-x-1">
             <img src="~/assets/images/update.png" class="w-6 h-6" alt="">
             <p class="edit-text">Edit Profile</p>
    </div> 

    </div>
 

    </div>
    </div>
</template>

<script>
import image from '~/assets/images/arrow-left.png'

  export default {
    data() {
        return {
            image,
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
.profile-container {
  padding: 0 10px 10px 10px;
  background-color: #fff;
  margin-top: 25px;
  border: 1px solid #E0E0E0;
  border-radius: 4px;

}
.profile-wrapper {
  
  display: flex;
  // flex-wrap: wrap;
  justify-content: space-between;
 
}
.profile-content {
  width: 60%;
  display: flex;
  justify-content: space-between;
}
.detail-title {
  font-size: 11px;
  font-weight: 400;
  color: #7A7A7A;
}
.detail-info {
  font-size: 14px;
  color: #292929;
  font-weight: 600;
}
// .profile-photo {
//   width: 200px;
//   height: 200px;
//   background-color: red;
//   border-radius: 50%;
// }
.detail-wrapper {
  margin-top: 1rem;
}

.active {
  color: #03A300;
  background-color: #EBFFEB;
  border-radius: 4px;
  text-align: center;
  width: 120px;
  font-weight: 600;
}
.edit {
  display: flex;
  justify-content: end;
  align-items: center;
  // padding: 10px 20px;
}
.edit-text {
  color: #516563;
  font-size: 400;
  font-size: 14px;
}


</style>