<template>
  <div class="mt-3">
    <v-row justify="center">
      <v-expansion-panels inset>
        <v-expansion-panel v-for="header in headers" :key="header">
          <v-expansion-panel-header>
            {{ header }}
            <!-- <span>
            25th July 2022 11:59am
          </span> --> 
          </v-expansion-panel-header>

          <v-expansion-panel-content>
              <div class="panel-wrapper">

                <div class="items-wrapper" >
                  <div class="items">
                    <h2 class="item-title">Observation</h2>
                     <ul>
                    <li>High Temprature</li>
                    <li>Flu</li>
                    <li>Head-aches</li>
                  </ul>
                  </div>

                  <div class="items">
                    <h2 class="item-title">Doctors Comment</h2>
                    <p class="item-text">Patient has to be tested at the lab and should be admitted for observation immediately</p>
                  </div>

                  <div class="items">
                    <h2 class="item-title">Drug Prescription</h2>
                    <ul>
                      <li>Paracetamol</li>
                      <li>Coatem 80-480</li>
                    </ul>
                  </div>
                 


                </div>
              <!-- <div
                v-for="content in contents"
                :key="content.listHeader"
                class="content"
              >
                <p class="list-header">{{ content.listHeader }}</p>
                <p class="list-text list--item">{{ content.itemText }}</p>
                <li class="item-list list--item">{{ content.itemOne }}</li>
                <li class="item-list list--item">{{ content.itemTwo }}</li>
                <li class="item-list list--item">{{ content.itemThree }}</li>
              </div> -->
            </div>
            
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      headers: [
        'Dr Abdulahi Abubaker',
        'Dr Abdulahi Abubaker',
        'Dr Abdulahi Abubaker',
        'Dr Abdulahi Abubaker',
        'Dr Abdulahi Abubaker',
      ],

     
    }
  },
}
</script>

<style lang="scss" scoped>
// .panel-wrapper {
//   display: flex;
 
//   width: 100%;
  
// }
.items-wrapper {
  display: flex;
  justify-content: space-between;
  width: 85%;
  
}
.item-title{
  font-size: 14px;
  color: #283231;
  font-weight: 600;
}
.item-text {
  width: 300px;
   font-size: 12px;
  color: #3D4C4A;
  margin-top: 10px;
}
li {
  list-style: disc;
  font-size: 12px;
  color: #3D4C4A;
  margin-top: 10px;
}


.v-expansion-panel-header {
  font-size: 14px;
  color: #292929;
  font-weight: 600;
  border: 1px solid #e0e0e0;
  border-radius: 5px;
  // border-top: none;
  padding: 0 10px;
}
.theme--light.v-expansion-panels .v-expansion-panel {
  margin-bottom: 10px;
}
.v-expansion-panel:not(:first-child)::after {
  border-top: none;
}
.content:nth-child(3) {
  margin-left: 100px;
}
.theme--light.v-expansion-panels .v-expansion-panel {
  box-shadow: none;
}

.v-expansion-panel--active > .v-expansion-panel-header {
  // background-color: red;
  min-height: 50px;
  margin-bottom: 20px;
  border: none;
  border-radius: 0;
  // border: 1px solid #799794;
  // border-bottom: 10px solid #fafafa;



}
.v-expansion-panels {
  padding: 0 11px;
}





.v-expansion-panel::before {
  box-shadow: none;
  border-radius: 10px;
}


</style>
