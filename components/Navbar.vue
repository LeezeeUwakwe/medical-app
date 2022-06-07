<template>
  <div class="nav-bar">
    <div class="navbar-container">
      <nav class="">
        <nuxt-link to="/">Overview</nuxt-link>

        <div class="dropdown">
          <div class="dropdown-wrapper" @click="openDropdown">
           <button ref="btnBtn" class="btn btn-patient">Patient</button>
           <img :src="`/${showDropdown ? 'dark-arrow' : 'light-arrow'}.png`" alt="">
          </div>
          <div v-if="showDropdown" class="dropdown-content">
            <nuxt-link to="/Patient" class="d-content">All Patients</nuxt-link>
            <nuxt-link to="/Appointments" class="d-content appointments">Appointments</nuxt-link>
          </div>
        </div>

        <nuxt-link to="/Staffs">Staffs</nuxt-link>

         <div class="dropdownPharm"> 
          <div class="dropdownPharm-wrapper" @click="openPharm">
           <button ref="btnTwo" class="btn btn-patient">Finance</button>
           <img :src="`/${showPharmacy ? 'dark-arrow' : 'light-arrow'}.png`" alt="">
          </div>
          <div v-if="showPharmacy" class="dropdownPharm-content">
          
            <nuxt-link to="/PatientReport" class="d-content">Patient Report</nuxt-link>
            <nuxt-link to="/HmoSettlement" class="d-content">HMO Settlement</nuxt-link>
            <nuxt-link to="#" class="d-content">Staff Payroll</nuxt-link>
            <nuxt-link to="/PharmacyReport" class="d-content">Pharmacy Report</nuxt-link>
            <nuxt-link to="/LabReport" class="d-content">Lab Report</nuxt-link>
          </div>
        </div>    
        <nuxt-link to="/Pharmacy">Pharmacy</nuxt-link>
        <nuxt-link to="/Analytics">Analytics</nuxt-link>
        <nuxt-link to="/Labs">Labs</nuxt-link>
        <nuxt-link to="/Users">Users</nuxt-link>
      </nav>
      <div class="admin">
        <img
          class="admin-image"
          src="~/assets/images/admin.png"
          alt=""
        />
        <p class="admin-text">Super Admin</p>
        <img src="~/assets/images/Vector (11).png" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showDropdown: false,

      showPharmacy: false,

      arrowDown: false,
      
    
    }
  },
  methods: {
    openDropdown() {
      this.showDropdown = !this.showDropdown;
      this.$refs.btnBtn.classList.toggle('btn-active');
    },

    openPharm() {
    this.showPharmacy = !this.showPharmacy;
    this.$refs.btnTwo.classList.toggle('btn-active');
  },
  
  },

}

</script>

<style scoped>


.nav-bar {
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.12);
  background-color:#fff;
  position: fixed;
  top: 0;
  right: 0;
  width: 100%;
  z-index: 10;
}

.navbar-container {
  display: flex;
  justify-content: end;
  align-items: center;
  padding: 14px 20px;
  margin: 0 2rem;
}
nav {
  display: flex;
  margin-right: 7rem;
  align-items: center;
  position: relative;
}
nav a {
  position: relative;
  color: #7a7a7a;
  font-weight: 400;
  font-size: 13px;
  margin-left: 2.5rem;
  height: 20px;
  box-sizing: border-box;
  text-decoration: none;
  align-items: center;

}
.admin {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 130px;
}
.admin-image {
  width: 30px;
  height: 30px;
}
.admin-text {
  font-size: 12px;
}
.v-application {
    font-family: "Avenir LT Std";

}
.v-application p {
    margin-bottom: 0;
}
.btn {
   border: none;
   outline: none;
}
.btn-patient {
  color: #7A7A7A; 
  font-size: 13px;
  height: 20px;
  box-sizing: border-box;

}
.dropdown,
.dropdownPharm {
 
  margin-left: 2.5rem;
  /* margin-bottom: 10px; */
}
.dropdown-wrapper,
.dropdownPharm-wrapper {
  display: flex;
  align-items: center;

}
.dropdown-content,
.dropdownPharm-content {
  background-color: #fff;
  position: absolute;
  top: 48px;
  display: flex;
  flex-direction: column;
  box-shadow: 0px 0px 4px 2px rgba(121, 151, 148, 0.16);
  height: 90px;
  z-index: 2;
  width: 122px;
}
.dropdownPharm-content {
  height: auto;
  padding-bottom: 17px;
  width: 130px;
}
.d-content {
  margin-left: 1rem;
  margin-top: 15px;
  color: #3D3D3D;
}
.d-content.nuxt-link-exact-active {
  color: #3D3D3D;
  font-weight: 400;
}
.btn-active {
  color: #283231;
  font-weight: 600;
}
.appointments {
  margin-top: 15px;
}
.nuxt-link-exact-active {
  color: #283231;
  font-weight: 600;
}
.nuxt-link-exact-active::after,
.btn-active::after {
    content: "";
    width: 38px;  
    display: block;
    justify-content: center;
    height: 3px;
    background: #283231;
    margin: 1rem auto;
}
.d-content.nuxt-link-exact-active::after {
  width: 0;
  height: 0;
}



</style>
