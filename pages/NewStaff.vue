<template>
  <div>
    <div class="container">
     <h1 class="newStaff-title mt-12">New Staff</h1>

      <nuxt-link 
      :src="image" 
      tag="img" 
      to="/Staffs"
      class="icon-left">
    </nuxt-link>

  
    <div class="input-wrapper">
        <BaseInput
           id="first-name"
          v-model="firstName"
          class="mb-3 input-field"
          type="text"
          label="First Name"/>
            <BaseInput
           id="last-name"
          v-model="lastName"
          class="mb-3 input-field"
          type="text"
          label="Last Name"/>

           <BaseInput
           id="position"
          v-model="position"
          class="mb-3 input-field"
          type="text"
          label="Position"/>

          <BaseInput
           id="gender"
          v-model="gender"
          class="mb-3 input-field"
          type="text"
          label="Gender"/>

            <BaseInput
           id="email"
          v-model="email"
          class="mb-3 input-field"
          type="text"
          label="Email Address"/>

            <BaseInput
           id="number"
          v-model="number"
          class="mb-3 input-field"
          type="number"
          label="Phone Number"/>

            <BaseInput
           id="residentialAddress"
          v-model="residentialAddress"
          class="mb-3 input-field"
          type="text"
          label="Residential Address"/>
          
            <BaseInput
           id="yearEmployed"
          v-model="yearEmployed"
          class="mb-3 input-field"
          type="year"
          label="Year Employed"/>

          
    </div>

      <div class="profile-wrapper">
      <nuxt-link to="/Profile" class="create">Create Profile</nuxt-link>
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
.newStaff-title {
   color: #292929;
  font-size: 20px;
  font-weight: 600;
}
.icon-left {
  margin-top: 18px;
  width: 25px;
  height: 25px;
}
.profile-wrapper {
   display: flex;
  justify-content: end;
  background-color: #FAFAFA;
  margin: 25px 0 0 0;
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
  width: 42%;
}

.input-wrapper {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 20px 60px;
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