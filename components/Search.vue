<template>
  <div class="search-wrapper">
   <div class="input-wrapper">
        <img class="mr-1" src="~/assets/images/search.png" alt="search-icon">
        <label for="search"></label>
        <input id="search" type="text" name="search" v-bind="$attrs">
      </div>
  </div>
</template>

<script>
export default {
  props: {
    search: {
      type: String,
      default: "",
    },
  },

  data: () => ({ }),
}
</script>

<style lang="scss" scoped>
.input-wrapper {
  background-color: #FFFFFF;
  display: flex;
  align-items: center;
  border: 0.5px solid #E0E0E0;
  border-radius: 6px;
  padding: 8px 15px;
  width: 320px;
}
input {
  width: 100%;
  outline: none;
}
.input-wrapper img {
  width: 20px;
  height: 20px;
}
::placeholder {
  color: #7A7A7A;
  font-weight: 400;
  font-size: 14px;
}

</style>