<template>
      <div class="today-wrapper space-x-2">
        <p class="today-text">Today</p>
        <img src="~/assets/images/arrow-down.png" class="" alt="arrow-down">
      </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>
.today-wrapper {
  background-color: #E4EAEA;
  color:  #525252;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 4.688rem;
  height: 2rem;
  padding: 3px 6px;
  border-radius: 6px;
  margin-left: 20px;
}
.today-text {
  font-size: 12px;
  font-weight: 600;
  margin-right: 5px;
}
.v-application p {
  margin-bottom: 0;
}

</style>