<template>
 <div class="mt-12">
    <v-row justify="center">
    <v-expansion-panels inset>
    <v-expansion-panel
    v-for="header in headers"
   :key="header"
    >
        <v-expansion-panel-header>
           {{header}}
        
            <!-- <span>
            25th July 2022 11:59am
          </span> -->
        </v-expansion-panel-header>
       
        <v-expansion-panel-content>
            <div class="update space-x-1">
             <img src="~/assets/images/update.png" alt="">
             <p class="update-text">Update</p>
           </div>
          <div class="panel-wrapper space-y-8">
            
           <div class="numbering-wrapper">

             <div class="numbering">
              <div class="circle"><p class="three circle-content">3</p></div>
              <div class="line"></div>
              <div class="circle"><p class="two circle-content">2</p></div>
              <div class="line"></div>
              <div class="circle"><p class="one circle-content">1</p></div>
              </div>

            <div>
            <div
           v-for="content in contents"
            :key="content.listHeader"
            class="content ml-8">

           
               <div class="date-wrapper space-x-1"> 
               <p class="list-header">{{content.listHeader}}</p>
               <p class="list-text list--item">{{content.date}}</p>
            </div>
          <div class="result-wrapper space-x-2 mb-10">
          <li class="item-list list--item test">{{content.test}}</li>
          <li class="item-list list--item">{{content.result}}</li>
          <li class="item-list list--item">{{content.resultOne}} <span class="item-list list--item result-two" >{{content.resultTwo}}</span></li>
          </div>
          <!-- <li "></li> -->
           
          </div>
          </div>
         

              </div>

               <!-- <div class="count-wrapper">
              <p
              v-for="count in 3" :key="count"
              class="circle-conten">{{count}}</p>
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
    

    data () {
      return {
        
         headers: [
                "Test and Results",
                "Medication",
                "Illness Record",
                "Scans",
          ],

          contents: [
            {
              listHeader: 'Hiv Test on ',
              date: '25th July, 2022 ',
              test: 'Result:',
              result: 'Negative',
            },
            {
              listHeader: 'Malaria and Typhoid Test on',
              date: '24th July, 2022',
              test: 'Result:',
              resultOne: 'Positive (Malaria++)',
              resultTwo: 'Positive (Typhoid)'
            },
            {
              listHeader: 'General Test on',
              date: '25th june, 2022',
              test: 'Result:',
              result: 'Positive (Malaria)'
            },

          ],
          count: "1",
        
          
           
        

        
      }
    }
    
  }
</script>

<style lang="scss" scoped>
.panel-wrapper {
  position: relative;
  // width: 90%;
  display: flex;
  flex-direction: column;
  // justify-content: space-between;
  // background-color: #E4EAEA;
}
.list-header{
  color: #283231;
  font-size: 14px;
  font-weight: 600;
  margin-bottom: 15px;
}
.list-text {
  width: 300px;
}
.list--item {
  font-size: 13px;
  color: #3D4C4A;
}
.result-two {
  display: block;
  // padding-left: 40px;
  padding-top: 5px;
  // color: red;
}

.test {
  color: #283231;
  font-weight: 600;
}
.v-expansion-panel-header {
  font-size: 14px;
  color: #292929;
  font-weight: 400;
}
// .content:nth-child(3) {
//  margin-left: 100px
// }
// .theme--light.v-expansion-panels .v-expansion-panel {
//   margin-top: 7px;
//   box-shadow: none;
// }
.update {
  display: flex;
  justify-content: end;
  align-items: center;
  padding: 10px 20px;
}
.update-text {
  color: #799794;
  font-size: 400;
  font-size: 14px;
}
.date-wrapper {
  display: flex;
  align-items: baseline;
}
.result-wrapper {
  display: flex;
}
.line {
  background-color: #516563;
  height: 80px;
  width: 1px;
}
// .numbering-wrapper {
//   display: flex;
//   flex-direction: column;
// }
.numbering {
  display: flex;
  align-items: center;
  flex-direction: column;
  max-width: fit-content;
}
.numbering-wrapper {
  display: flex;
}
.circle {
  width: 30px;
  height: 30px;
  background-color: #516563;
  border-radius: 50%;
 
  // padding: 5px;
}
.circle-content {
  color: #fff;
  text-align: center;
  padding-top: 3px;
  font-size: 15px;  
}
.circle-conten {
  color: red;
  margin-top: 20px;
}
.count-wrapper {
  display: flex;
  flex-direction: column-reverse;
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

.v-tabs-slider{
    background-color: red;
    height: 100%;
    width: 40% !important;
}
</style>
