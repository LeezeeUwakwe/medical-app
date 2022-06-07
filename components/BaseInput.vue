<template>
  <div class="">
    <div class="">
   <label v-if="label" :for="id" class="label-text">
      {{ label }}
    </label>
    <input
      :id="id"
      :type="type"
      :value="modelValue"
      class="border p-1 field"
      v-bind="$attrs"
      @input="updateInput"
    />
    </div>
  </div>
</template>

<script>
export default {

  props: {
    id: {
      type: String,
      default: "",
    },
    label: {
      type: String,
      default: "",
    },
    modelValue: {
      type: [String, Number],
      default: "",
    },
    type: {
      type: String,
      default: "text",
    }
  },
  methods: {
    updateInput(event) {
      this.$emit("update:modelValue", event.target.value);
    }
  }
};
</script>


<style lang="scss" scoped>
.field {
  border: 0.094rem solid #666;
  border-radius: 5px;
  padding: 10px 4px;
  width: 100%; 
  outline: none;
  background-color: #F6F8F9;
}
input[type="date"] {
   font-size: 10px; 
   padding: 12px 4px;
}

.label-text {
  font-size: 12px;
  font-weight: 600;
  color: #3D3D3D;
}
label {
  // color: #525252;
  color: red;
  font-weight: 600;
}

</style>