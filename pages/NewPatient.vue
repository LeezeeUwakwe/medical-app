<template>
  <div>
    <Navbar />
    <!-- <NavBBar /> -->
    <div class="container">
      <h1 class="newPatient-title">New Patient</h1>

      <nuxt-link 
      :src="image" 
      tag="img" 
      to="/Patient"
      class="mt-6 w-7 h-7">
    </nuxt-link>

    <Tab />
      




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
.newPatient-title {
   color: #292929;
  font-size: 20px;
  font-weight: 600;
  margin-top: 40px;
}

</style>