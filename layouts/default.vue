<template>
  <v-app dark>

    
    <v-main>
      <Navbar />
      <div class="nuxt-wrapper">
        <v-container>
        <Nuxt />
      </v-container>
      </div>
      
    </v-main>
   
   
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
    }
  },
}
</script>

<style lang="scss" scoped>

.nuxt-wrapper {
  background-color: #FAFAFA;
  font-family: "Avenir LT Std";
  min-height: 100vh;
}
.v-application {
  font-family: "Avenir LT Std";

}
</style>
