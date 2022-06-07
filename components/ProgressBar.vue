<template>
  <div>
    <div class="progress-wrapper">
      
    <div class="details-wrapper">
      <h2 class="text">Reliance HMO</h2>
      <p class="details">15,000 Patients(32%)</p>
    </div>
    <v-progress-linear
      color="#EE6C4D"
      rounded
      value="30"
      class="linear-1"
      style="height: 2px;"
    ></v-progress-linear>
    <br>
     <div class="details-wrapper">
      <h2 class="text">Ajocard</h2>
      <p class="details">15,000 Patients(32%)</p>
    </div>
    <v-progress-linear
      color="#662C91"
      rounded
      value="100"
       style="height: 2px;"

    ></v-progress-linear>
    <br>
     <div class="details-wrapper">
      <h2 class="text">AXA</h2>
      <p class="details">15,000 Patients(32%)</p>
    </div>
    <v-progress-linear
      color="#A8201A"
      rounded
      value="100"
      style="height: 2px;"

    ></v-progress-linear>
    <br>
     <div class="details-wrapper">
      <h2 class="text">Healthpoint HMO</h2>
      <p class="details">15,000 Patients(32%)</p>
    </div>
    <v-progress-linear
      color="#F38D68"
      rounded
      value="100"
      style="height: 2px;"

    ></v-progress-linear>
    <br>
     <div class="details-wrapper">
      <h2 class="text">Hallmark</h2>
      <p class="details">15,000 Patients(32%)</p>
    </div>
      <v-progress-linear
      color="#FF1053"
      rounded
      value="100"
      style="height: 2px;"

    ></v-progress-linear>
    <br>
     <div class="details-wrapper">
      <h2 class="text">Metrohealth</h2>
      <p class="details">15,000 Patients(32%)</p>
    </div>
    <v-progress-linear
      color="#F7EC59"
      rounded
      value="100"
       style="height: 2px;"

    ></v-progress-linear>
   
   
  </div>

  </div>
</template>

<script>
  export default {
    data () {
      return {
        valueDeterminate: 50,
      }
    },
  }
</script>

<style lang="scss" scoped>
.progress-wrapper {
  margin: 22px 0 10px 0;

}
.details-wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #516563;
  padding: 0 15px 4px 15px;
}
.text {
  font-size: 11px;
  font-weight: 400;
}
.details {
  font-size: 11px;
  font-weight: 400;
}
.v-application p {
  margin-bottom: 0;
}
.v-progress-linear__determinate::v-deep {
  height: 1px;
}
</style>