<template>
  <div>
    <div class="container">
    <div class="user-header">
    <h1 class="user-title">Users</h1>
    <div class="user-content space-x-7">
       <Search
          :search="search" 
          class="mt-1"
          placeholder="Search"
        />      
        <Today-btn />

        <nuxt-link to="/NewUser" class="new-user">New User</nuxt-link>


    </div>
   </div>

    <div class="w-1/5"> 
     <Card :cards="cards" />
   </div>

     <div class="user-table">
        <h2 class="user-list mt-6">Users List</h2>
        <UserTable />

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
          title: "Total Users",
          numbers:"1,000,000",
        },
        ]
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
.user-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 5.5rem;
}
.user-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.new-user {
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
.user-title {
  color: #292929;
  font-size: 25px;
  font-weight: 600;
}
.user-list {
  font-size: 14px;
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