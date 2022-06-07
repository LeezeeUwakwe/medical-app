<template>
  <div>
      <div class="container">
        <div class="today-container">
          <div class="today-wrapper">
        <Today-btn />
        </div>
        </div>
      

        <AnalyticsTab />

      </div>
  </div>
</template>

<script>
  export default {
}
</script>

<style lang="scss" scoped>
.container {
   padding: 2rem;
   margin: 0 auto; 
   margin-bottom: 4rem;
}
.today-container {
  display: flex;
  justify-content: flex-end;
  margin-top: 45px;
}

</style>