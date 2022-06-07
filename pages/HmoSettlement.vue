<template>
  <div>
    <div class="container">
  <div class="hmo-header">
    <h1 class="hmo-title">HMO Settlement</h1>
     
    <div class="hmo-content space-x-7">
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
        <h2 class="hmo-list">Recognized HMO List</h2>
         <HmoTable />
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
                    icon: "/house-icon.png",
                    title: "Recognized HMOs",
                    numbers: "1,000",
                },
                {
                    icon: "/icon.png",
                    title: "Income from HMO",
                    numbers: "N1,000,000",
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
.hmo-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 5.5rem;
}
.hmo-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.hmo-title {
  color: #292929;
  font-size: 25px;
  font-weight: 600;
}
.hmo-list {
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