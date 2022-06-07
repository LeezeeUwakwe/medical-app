<template>
  <div>
      <div class="newConsult-wrapper">
        <h1 class="observe-title">Observation</h1>
         <Search
          :search="search" 
          class="mt-1"
          placeholder="Search for symptoms"
        /> 
         <ComboBox
         class="mt-1
         w-full" />
         <div class="doctor-drug">
           <div class="doctor">
             <h1 class="text-title"> Doctors Comment</h1>
             <label for="comment"></label>
             <textarea id="comment" name="comment" cols="30" rows="8" class="text-area w-full mt-2 bg-white"></textarea>
           </div>
           <div class="drug">
             <h1 class="text-title">Drug prescription</h1>
             <div class="drug-wrapper">
                 <Search
          :search="search" 
          class="mt-2"
          placeholder="Search for drugs"
        />  
        <ComboBoxx
        class="mt-3 w-full" />
             </div>
           </div>
         </div>
      </div>
  </div>
</template>

<script>
  export default {
}
</script>

<style lang="scss" scoped>

.observe-title,
.text-title {
   font-size: 14px;
   color: #292929;
   font-weight: 600;
}
.doctor,
.drug {
  width: 49%;
}
.doctor-drug {
  display: flex;
  justify-content: space-between;
}
textarea {
  border: 1px solid #E0E0E0;
  resize: none;
  border-radius: 4px;
  
}


</style>