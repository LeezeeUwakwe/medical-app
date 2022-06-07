<template>
  <div>
    <div class="container">

      <h2 class="meds mt-6"> Paracetamol</h2>

      <nuxt-link 
      :src="image" 
      tag="img" 
      to="/NewMedication"
      class="mt-6 w-7 h-7">
    </nuxt-link>
    <div class="add-container">
        <div class="add-content">

          <div>
            <h2 class="content-title">Price</h2>
            <p class="content-text">N4,000</p>
          </div>

          <div>
            <h2 class="content-title">Category</h2>
            <p class="content-text">Analgesics and antipyretics</p>
          </div>

          <div>
            <h2 class="content-title">Quantity Available</h2>
            <p class="content-text">150</p>
          </div>

          <div class="available-wrapper space-x-1">
            <p class="available text-sm">Available</p>
            <img src="~/assets/images/arrow-down.png" class="arrow-down p-1 rounded" alt="">
          </div>


        </div>

          <div class="edit space-x-1 mt-16">
             <img src="~/assets/images/update.png" class="w-6 h-6" alt="">
             <p class="edit-text">Edit Medication</p>
    </div> 
      </div>

    </div>
    </div>
  
</template>

<script>
import image from '~/assets/images/arrow-left.png'

  export default {
    data () {
      return {
        image,
      }
    }
    
  }
</script>

<style lang="scss" scoped>
 .container {
  .container {
   padding: 2rem;
   margin: 0 auto; 
   margin-bottom: 4rem;
}
}
.meds {
  font-size: 22px;
  color: #292929;
  font-weight: 600;
}
.add-container {
  padding: 25px;
  background-color: #fff;
  margin-top: 25px;
  border: 1px solid #E0E0E0;
  border-radius: 4px;
  height: 30vh;
}

.add-content {
  // width: 60%;
  display: flex;
  justify-content: space-between;
}
.available-wrapper {
  display: flex;
  align-items: center;
}
.content-title {
  font-size: 11px;
  color: #7A7A7A;
}
.content-text {
  color: #292929;
  font-size: 15px;
  margin-top: 3px;
}
.available {
  color: #03A300;
  background-color: #EBFFEB;
  border-radius: 4px;
  text-align: center;
  width: 120px;
  font-weight: 400;
  padding: 7px 10px;
}
.arrow-down {
  background-color: #F5EFEE;
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
.v-application p {
  margin-bottom: 0;
}



</style>