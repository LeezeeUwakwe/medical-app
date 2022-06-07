<template>
  <div>
    <div class="nav-container">
     <div class="nav-wrapper">
      <div class="nav-bar">
        <div id="nav-wrapper" ref="navWrapper" class="unordered-wrapper">

          <p class="unordered-item" @click="addClass">
            <nuxt-link id="overview" to="/"> Overview</nuxt-link>
          </p>

          <p id="patients" ref="btnBtn" class="unordered-item btn-patient" @click="addClass">Patients</p>
          <!-- <span class=""><img :src="`/${activeIcon ? 'dark-arrow' : 'light-arrow'}.png`" alt=""></span> -->
          
          <p id="staffs" class="unordered-item" @click="addClass">
           <nuxt-link to="/Staffs">Staffs</nuxt-link>
          </p>

          <p id="finance" ref="btnBtn" class="unordered-item btn-finance" @click="addClass">Finance</p>
          <!-- <span class=""><img :src="`/${activeIcon ? 'dark-arrow' : 'light-arrow'}.png`" alt=""></span> -->
          <p id="pharmacy" class="unordered-item" @click="addClass">Pharmacy</p>

          <p id="analytics" class="unordered-item" @click="addClass">
            <nuxt-link to="/Analytics">Analytics</nuxt-link> 
          </p>

          <p id="labs" class="unordered-item" @click="addClass">Labs</p>
          <p id="users" class="unordered-item" @click="addClass">Users</p>

        </div>
      </div>


      <div class="super space-x-1">
        <img class="super-img" src="~/assets/images/admin.png" alt="">
          <p class="superAdmin-text">Super Admin</p>
          <img class="arrow-admin" src="~/assets/images/dark-arrow.png" alt="">
      </div>

      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        activeIcon : false,
        // activeIconn : false,
      }
    },
    
    methods: {
      addClass(e) {
        const element = document.getElementById('nav-wrapper');
        const children = element.children;
        
        for(let i = 0; i<children.length; i++) {
          const child = children[i];
          if (child.id === e.target.id) {
            child.classList.add('active-class') 
          } else {
            child.classList.remove('active-class')
          }
        }
       this.activeIcon = !this.activeIcon;
      //  this.activeIconn = !this.activeIconn
    }
        

      
        
    }
  }

    
    
  
</script>

<style lang="scss" scoped>
.nav-container {
  width: 100%;
  height: 55px;
  padding: 0 3rem;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.12);
  background-color:#fff;
}
.nav-wrapper {
  max-width: 90%;
  display: flex;
  align-items: center;
}
.unordered-wrapper {
  display: flex;
  margin-right: 7rem;
  align-items: center ;
}
.unordered-item {
  color: #7a7a7a;
  font-weight: 400;
  font-size: 13px;
  margin-left: 3rem;
  cursor: pointer;
  height: 20px;
  box-sizing: border-box;
}
.super {
  display: flex;
  align-items: center;
}

.superAdmin-text {
  font-size: 12px;
  color: #000000;
}
.super-img {
  width: 25px;
  height: 25px;
}
.active-class {
  color: #283231;
  // color: red;
  font-weight: 600;
}
.active-class::after {
   content: "";
    width: 38px;  
    display: block;
    justify-content: center;
    height: 3px;
    background: #283231;
    margin: 1rem auto;
}
.light-arrow,
.dark-arrow {
  margin-top: 2px;
  width: 17px;
  height: 17px;

}
.arrow-admin {
  width: 17px;
  height: 17px;
}

</style>