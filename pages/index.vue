<template>
  <div class="">
    <div class="container">
      <div class="hero relative">
        <div class="rectangle">
          <div class="greeting">
            <h1 class="welcome-text">Welcome Back, {{name}}.</h1>
            <p class="welcome-date text-base">25th October, 2022</p>
          </div>          
          <div class="doctor-panel">
            <img src="~/assets/images/doctors.png" alt="">
          </div>
        </div>
      </div>
      
      <Card
      :cards="cards" />

      <div class="activities">
        <h1 class="activities-title">Activities</h1>
        <div class="api">
           <img class="" src="~/assets/images/api2.png" alt="">
        </div>
      </div>

      <div class="patient-queued mt-8 ">
        <div class="mt-2 list-header">
          <h2 class="patient-queued font-bold">Patients Queued</h2>
          <p class="view">View full list</p>
        </div>
          <Table :tables="tables" />
      </div>

    </div>
  </div>
</template>

<script>

export default {
    data() {
        return {
          name : 'Dave',
            cards: [
                {
                    icon: "/bed-frame.png",
                    title: "Patients Today",
                    numbers: "10,000",
                    subIcon: "/error-arrow.png",
                    subText: "15% today",
                    subColor: "warning"
                },
                {
                    icon: "/user.png",
                    title: "New Patients",
                    numbers: "10,000",
                    subIcon: "/success-arrow.png",
                    subText: "15% today",
                    subColor: "success"
                },
                {
                    icon: "/bed-frame.png",
                    title: "Total Staff",
                    numbers: "10,000",
                },
                {
                    icon: "/icon.png",
                    title: "Profit This Month",
                    numbers: "10,000",
                    subIcon: "/success-arrow.png",
                    subText: "15% in february",
                    subColor: "success"
                },
                {
                    icon: "/user.png",
                    title: "Active Doctors",
                    numbers: "10,000",
                },
            ],
            tables: [
                {
                    // box: '',
                    id: 142314,
                    name: "Afolabi Oluwatobiloba",
                    email: "afolabitobi200@gmail.com",
                    gender: "Male",
                    age: "45",
                    time: "11.59pm",
                    icon: "/icon (2).png"
                },
                {
                    id: 142314,
                    name: "Afolabi Oluwatobiloba",
                    email: "afolabitobi200@gmail.com",
                    gender: "Male",
                    age: "45",
                    time: "11.59pm",
                    icon: "/icon (2).png"
                },
                {
                    id: 142314,
                    name: "Afolabi Oluwatobiloba",
                    email: "afolabitobi200@gmail.com",
                    gender: "Male",
                    age: "45",
                    time: "11.59pm",
                    icon: "/icon (2).png"
                },
                {
                    id: 142314,
                    name: "Afolabi Oluwatobiloba",
                    email: "afolabitobi200@gmail.com",
                    gender: "Male",
                    age: "45",
                    time: "11.59pm",
                    icon: "/icon (2).png"
                },
                {
                    id: 142314,
                    name: "Afolabi Oluwatobiloba",
                    email: "afolabitobi200@gmail.com",
                    gender: "Male",
                    age: "45",
                    time: "11.59pm",
                    icon: "/icon (2).png"
                },
                {
                    id: 142314,
                    name: "Afolabi Oluwatobiloba",
                    email: "afolabitobi200@gmail.com",
                    gender: "Male",
                    age: "45",
                    time: "11.59pm",
                    icon: "/icon (2).png"
                },
                {
                    id: 142314,
                    name: "Afolabi Oluwatobiloba",
                    email: "afolabitobi200@gmail.com",
                    gender: "Male",
                    age: "45",
                    time: "11.59pm",
                    icon: "/icon (2).png"
                },
                {
                    id: 142314,
                    name: "Afolabi Oluwatobiloba",
                    email: "afolabitobi200@gmail.com",
                    gender: "Male",
                    age: "45",
                    time: "11.59pm",
                    icon: "/icon (2).png"
                },
                {
                    id: 142314,
                    name: "Afolabi Oluwatobiloba",
                    email: "afolabitobi200@gmail.com",
                    gender: "Male",
                    age: "45",
                    time: "11.59pm",
                    icon: "/icon (2).png"
                },
                {
                    id: 142314,
                    name: "Afolabi Oluwatobiloba",
                    email: "afolabitobi200@gmail.com",
                    gender: "Male",
                    age: "45",
                    time: "11.59pm",
                    icon: "/icon (2).png"
                },
            ],
        };
    },
}

</script>

<style scoped>

.container {
   padding: 2rem;
   margin: 0 auto; 
   margin-bottom: 4rem;
}
.hero {
  position: relative;
}
.rectangle {
  background-color: #E4EAEA;
  height: 4.375rem;
  margin-top: 6.6rem ;
  padding: 0 6.3rem;
  /* padding-bottom: 2px; */
}
.greeting {
 padding-top: 8px;
}
.welcome-text {
  font-size: 22px; 
  color: #283231;
  font-weight: 600;
}
.welcome-date {
  color: #799794;
  font-size: 12px;
}
.doctor-panel {
  position: absolute;
  bottom: -25px;
  right: 36px;
  /* width: 270px; */
}
.doctor-panel img {
  width: 270px;
}
.warning {
  color: #CC0000;
  font-size: 12px;
  font-weight: 600;
}
.success {
  color: #03A300;
  font-size: 12px;
  font-weight: 600;
}
.list-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-bottom: 0;
}
.view {
  font-size: 12px;
  color: #799794;
  border-bottom: 1px solid #799794;
  font-weight: 200;
}
.activities {
  margin-top: 30px
}
.activities-title,
.patient-queued {
   font-size: 15px;
   color: #292929;
}
.api {
  width: 100%;
  margin-top: 6px;
}
.api img {
  max-width: 100%;
}
table.v-table thead th {
  font-size: 20px !important;
  font-weight: 600;
 }
.v-application p {
  margin-bottom: 0;
}

</style>
