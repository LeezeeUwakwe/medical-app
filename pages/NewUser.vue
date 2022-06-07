<template>
  <div>
    <div class="container">
        <h1 class="newUser-title mt-12">New User</h1>
      <nuxt-link 
      :src="image" 
      tag="img" 
      to="/Users"
      class="icon-left mt=6">
    </nuxt-link>

    <div class="input-wrapper">
      <div class="input-contents">

         <BaseInput
           id="name"
          v-model="Name"
          class="mb-3 input-field"
          type="text"
          label="Name"/>
            <BaseInput
           id="email"
          v-model="email"
          class="mb-3 input-field"
          type="email"
          label="Email Address"/>

           <BaseInput
           id="role"
          v-model="role"
          class="mb-3 input-field"
          type="text"
          label="Role"/>

                </div>


    <div class="permissions-wrapper">
        <h3 class="permissions">Permissions</h3>
        <div class="checkbox-container">
          <div class="top">

            <div class="checkbox-wrapper">
          <input id="bio-data" type="checkbox" name="bio-dat" value="patient bio-data">
         <label for="bio-data" class="checkbox-label"> Edit patient bio-data</label>
          </div>

           <div class="checkbox-wrapper">
          <input id="medical-history" type="checkbox" name="medical-history" value="patient medical history">
         <label for="medical-history" class="checkbox-label"> Edit patients medical history</label>
          </div>

          <div class="checkbox-wrapper">
          <input id="hmo-tier" type="checkbox" name="hmo-teir" value="patients hmo tier">
         <label for="hmo-tier" class="checkbox-label"> Edit patients hmo tier</label>
          </div>

          <div class="checkbox-wrapper">
          <input id="consultation" type="checkbox" name="consultation" value="consultation">
         <label for="consultation" class="checkbox-label">Consultation</label>
         </div>

          <div class="checkbox-wrapper">
          <input id="reciept" type="checkbox" name="reciept" value="reciept">
         <label for="reciept" class="checkbox-label">Generate reciept</label>
         </div>

          </div>
          
        <div class="down">
           <div class="checkbox-wrapper">
          <input id="staff-details" type="checkbox" name="staff-details" value="staff-details">
         <label for="staff-details" class="checkbox-label">Edit staff details</label>
         </div>

          <div class="checkbox-wrapper">
          <input id="add-staff" type="checkbox" name="add-staff" value="add-staff">
         <label for="add-staff" class="checkbox-label">Add staff</label>
         </div>

          <div class="checkbox-wrapper">
          <input id="access" type="checkbox" name="access" value="access-finance">
         <label for="access" class="checkbox-label">Access to finance</label>
         </div>

          <div class="checkbox-wrapper">
          <input id="medication" type="checkbox" name="medication" value="Add Medication">
         <label for="medication" class="checkbox-label">Add medication</label>
         </div>

          <div class="checkbox-wrapper">
          <input id="edit-manage" type="checkbox" name="edit-manage" value="edit-manage">
         <label for="edit-manage" class="checkbox-label">Edit/manage medications</label>
         </div>

          <div class="checkbox-wrapper">
          <input id="access-analytics" type="checkbox" name="" value="access-analytics">
         <label for="access-analytics" class="checkbox-label">Access to analytics</label>
         </div>
          

        </div>
        
        </div>
        <div class="create-wrapper">
      <nuxt-link to="" class="create">Create User</nuxt-link>
    </div>
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

      }
    }
    
  }
</script>

<style lang="scss" scoped>
.container {
  padding: 2rem;
  margin: 0 auto; 
  margin-bottom: 4rem;
}

.newUser-title {
   color: #292929;
  font-size: 20px;
  font-weight: 600;
}
.icon-left {
  margin-top: 18px;
  width: 25px;
  height: 25px;
}
.input-field {
  width: 42%;
}


.input-wrapper {

  padding: 20px 60px;
  background-color: #fff;
  margin-top: 25px;
  border: 1px solid #E0E0E0;
  border-radius: 4px;
}
.input-contents {

  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  
}
.permissions {
  color: #292929;
  margin-top: 20px;
  font-weight: 600;
  font-size: 15px;
}
.top {
  margin-top: 8px;
  width: 75%;
  display: flex;
  justify-content: space-between;
}
.down {
  margin-top: 10px;
  width: 85%;
  display: flex;
  justify-content: space-between;
}
.top {
  width: 80%;
  display: flex;
  justify-content: space-between;
}

// input[type="checkbox"] {
//   visibility: hidden;
// }
// input[type="checkbox"] + label:before {
//   border-radius: 3px;
//   border: 1px solid #8F8F8F;
//   content: "\00a0";
//   display: inline-block;
//   font: 16px/1em sans-serif;
//   height: 16px;
//   margin: 0 .25em 0 0;
//   padding: 0;
//   // vertical-align: top;
//   width: 18px;
// }
// input[type="checkbox"]:checked + label:before {
//   background: #FFF;
//   color: #8F8F8F;
//   content: "\2713";
//   text-align: center;
// }
.checkbox-label {
  color: #3D3D3D;
  font-weight: 600;
  font-size: 12px;
  margin-bottom: 8px;
}

.create-wrapper {
   display: flex;
  justify-content: end;
  margin: 50px 0 30px 0;
}
.create {
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
a {
  text-decoration: none;
}

</style>