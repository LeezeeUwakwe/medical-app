<template>
  <vc-donut
    background="white" foreground="grey"
    :size="180" unit="px" :thickness="20"
    has-legend legend-placement="bottom"
    :sections="sections" :total="100"
    :start-angle="0" :auto-adjust-text-size="true" 
    >
    <h1 class="total-number text-sm">10,000,000</h1>
    <p class="total-text">Total Patients</p>
  </vc-donut>
</template>

<script>
  export default {
    data() {
      return {
        sections: [
          { label: 'Female',  value: 40, color: '#CDB1A8' },
          { label: 'Male', value: 60, color: '#799794' },       
]
      };
    },
 
  };
</script>

<style scoped>

.v-application p {
  margin-bottom: 0;
}

.cdc-legend-item {
  margin: 1.5em;
}
</style>