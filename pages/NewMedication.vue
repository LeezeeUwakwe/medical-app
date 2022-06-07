<template>
  <div>
    <div class="container">
     <h1 class="newMeds-title mt-6">New Medication</h1>

      <nuxt-link 
      :src="image" 
      tag="img" 
      to="/Pharmacy"
      class="mt-6 w-7 h-7">
    </nuxt-link>

   
    <div class="input-wrapper">
        <BaseInput
           id="name"
          v-model="Name"
          class="mb-3 input-field"
          type="text"
          label="Name"/>

            <BaseInput
           id="classification"
          v-model="classification"
          class="mb-3 input-field"
          type="text"
          label="Classification"/>

           <BaseInput
           id="price"
          v-model="price"
          class="mb-3 input-field"
          type="text"
          label="Price"/>

          <BaseInput
           id="quantity"
          v-model="quantity"
          class="mb-3 input-field"
          type="text"
          label="Quantity"/>

        
    </div>
     <div class="profile-wrapper">
      <nuxt-link to="/AddMedication" class="create">Add Medication</nuxt-link>
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
.newMeds-title {
   color: #292929;
  font-size: 20px;
  font-weight: 600;
}
.profile-wrapper {
   display: flex;
  justify-content: end;
  background-color: #FAFAFA;
  margin-top: 30px;

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
.input-field {
  width: 45%;
}

.input-wrapper {
  
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 20px 30px;
  background-color: #fff;
  margin-top: 25px;
  border: 1px solid #E0E0E0;
  border-radius: 4px;
}
.v-application p {
  margin-bottom: 0;
}
a {
  text-decoration: none;
}


</style>