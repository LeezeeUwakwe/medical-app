<template>
  <v-card>
    <v-tabs
v-model="tab" grow>
        <v-tabs-slider></v-tabs-slider>

      <v-tab v-for="item in items" :key="item">
        {{ item }}
      </v-tab>
    </v-tabs>
    <!-- Bio Data -->
    <v-tabs-items v-model="tab">

      <v-tab-item class="">
        <v-card flat class="">
          <div class="base-wrapper">
            <BaseInput
              id="first-name"
              v-model="firstName"
              class="mb-3 input-field"
              type="text"
              label="First Name"
            />

            <BaseInput
              id="last-name"
              v-model="lastName"
              class="mb-3 input-field"
              type="text"
              label="Last Name"
            />

            <BaseInput
              id="age"
              v-model="age"
              class="mb-3 input-field"
              type="number"
              label="Age"
            />

            <BaseInput
              id="gender"
              v-model="gender"
              class="mb-3 input-field"
              type="text"
              label="Gender"
            />

            <BaseInput
              id="height"
              v-model="height"
              class="mb-3 input-field"
              type="number"
              label="Height"
            />

            <BaseInput
              id="weight"
              v-model="weight"
              class="mb-3 input-field"
              type="text"
              label="Weight"
            />

            <BaseInput
              id="dob"
              v-model="dob"
              class="mb-3 input-field"
              type="date"
              label="Date Of Birth"
            />

            <BaseInput
              id="sob"
              v-model="sob"
              class="mb-3 input-field"
              type="text"
              label="State Of Birth"
            />

            <BaseInput
              id="email"
              v-model="email"
              class="mb-3 input-field"
              type="email"
              label="Email"
            />

            <BaseInput
              id="number"
              v-model="number"
              class="mb-3 input-field"
              type="number"
              label="Phone Number"
            />

            <BaseInput
              id="address"
              v-model="address"
              class="mb-3 input-field"
              type="text"
              label="Residential Address"
            />

            <BaseInput
              id="marital-status"
              v-model="maritalStatus"
              class="mb-3 input-field"
              type="text"
              label="Marital Status"
            />

            <BaseInput
              id="genotype"
              v-model="genotype"
              class="mb-3 input-field"
              type="text"
              label="Genotype"
            />

            <BaseInput
              id="blood-group"
              v-model="bloodGroup"
              class="mb-3 input-field"
              type="text"
              label="Blood Group"
            />
          </div>
          <div class="staff-wrapper">
            <nuxt-link to="/NewStaff" class="new-staff mt-6"
              >New Staff</nuxt-link
            >
          </div>
        </v-card>
      </v-tab-item>

      <!-- Medical History -->
      <v-tab-item>
        <v-card flat light>
          <MedicalHistory />
        </v-card>
      </v-tab-item>

      <!-- HMO -->
      <v-tab-item>
        <v-card flat>
          <div class="hmo-heading px-4 bg-white mt-6">
            <div class="update space-x-1">
              <img src="~/assets/images/update.png" class="w-5 h-5" alt="" />
              <p class="update-text">Update</p>
            </div>

            <div class="hmo-wrapper space-x-40 bg-white">
              <div>
                <h2 class="hmo-title">HMO Name</h2>
                <p class="hmo-text">Reliance HMO</p>
              </div>
              <div>
                <h2 class="hmo-title">HMO Type</h2>
                <p class="hmo-text">Private</p>
              </div>
            </div>

            <div class="py-4">
              <h2 class="hmo-title">HMO Teir</h2>
              <p class="hmo-text">Premium Individual</p>
            </div>
          </div>

          <div class="tier-wrapper">
            <h2 class="pl-4 hmo-title bg-white">Tier Benefits</h2>

            <ul class="list-wrapper">
              <li
                v-for="benefit in benefits"
                :key="benefit"
                class="item pt-5 ml-7"
              >
                {{ benefit.listItem }}
              </li>
            </ul>
          </div>
        </v-card>
      </v-tab-item>

      <!-- Finance -->
      <v-tab-item>
        <v-card flat>
          <div class="finance-wrappe">
            <div class="finance space-x-6">
              <Card :cards="cards" class="card-container" />
              <nuxt-link to="#" class="gen-receipt">Generate Receipt</nuxt-link>
            </div>
            <h1 class="receipt-history mt-4">Receipt History</h1>
          </div>
        </v-card>
      </v-tab-item>

      <!-- Consultation -->
      <v-tab-item>
        <v-card flat>
          <div class="consultation">
            <div class="consultation-wrapper">
              <button class="new-consultation mt-6" @click="consult = !consult">
                {{ consult ? 'New' : 'End' }} Consultation
              </button>
            </div>
            <Consulation v-if="consult" />
            <NewConsultation v-else />
            <!-- <div v-else></div> -->
          </div>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      consult: true,
      email: '',
      tab: null,
      items: ['Bio-Data', 'Medical History', 'HMO', 'Finance', 'Consultation'],
      // text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      benefits: [
        {
          listItem: 'Primary/Secondary Dental Care',
        },
        {
          listItem: 'Out Patient Care, General and Specialist Consultation',
        },
        {
          listItem: 'Minor, Intermediate, Major Surgeries and Procedures',
        },
        {
          listItem: 'Admissions (Including Feeding)',
        },
        {
          listItem:
            'Evacuation (Home/Hospital to Hospital & Road Side to Hospital)',
        },
        {
          listItem: 'X-Rays, Laboratory & Diagnostic Tests',
        },
        {
          listItem: 'Physiotherapy Sessions (Up to Approved Limits)',
        },
        {
          listItem: 'NPI Immunizations',
        },
        {
          listItem: 'Antenatal care, Induction of labour & Normal delivery',
        },
        {
          listItem:
            'Assisted delivery & Emergency or Medically indicated Elective Caesarean Section',
        },
        {
          listItem:
            'HIV/AIDS – to the Extent of Diagnosis + Treatment at Free Specialist Centres',
        },
        {
          listItem: 'Psychiatry Cover up to 8 Weeks',
        },
        {
          listItem:
            'Advanced and Complex Investigations (Including CT Scan, MRI Scan)',
        },
        {
          listItem: 'Treatment of ENT diseases and removal of foreign bodies',
        },
        {
          listItem: 'ENT Surgeries',
        },
      ],
      cards: [
        {
          icon: '/bed-frame.png',
          title: 'Total Due',
          numbers: '1,000,000',
        },
        {
          icon: '/bed-frame.png',
          title: 'Total Paid',
          numbers: '1,000,000',
        },
        {
          icon: '/bed-frame.png',
          title: 'Pending Payment',
          numbers: '1,000,000',
        },
        {
          icon: '/bed-frame.png',
          title: 'Covered by HMO',
          numbers: '1,000,000',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>

.v-tab::v-deep {
  text-transform: none;
  color: #7a7a7a;
  font-size: 13px;
  font-weight: 400;
  letter-spacing: 0;
}
.v-tabs-slider {
  background-color: #283231 !important;
  width: 20%;
  margin-left: 15%;
  height: 4px;
}

.theme--light.v-tabs > .v-tabs-bar .v-tab:not(.v-tab--active) {
  margin-left: -14px;
  padding-right: 85px;
}
.v-tab--active {
  color: #283231 !important;
  font-weight: 600;
  margin-left: -14px;
  padding-right: 85px;
  background-color: #FAFAFA;
}

.v-tabs--grow > .v-tabs-bar .v-tab {
  flex: none;
}

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
.hmo-title {
  font-size: 10px;
  color: #7a7a7a;
  font-weight: 400;
  background-color: #fff;
}
.hmo-text {
  font-size: 15px;
  color: #292929;
}
.hmo-wrapper {
  display: flex;
  align-items: center;
}
.v-sheet.v-card:not(.v-sheet--outlined) {
  box-shadow: none;
  border: 1px solid #fafafa;

  // background-color: #FAFAFA;
}

.theme--light.v-tabs::v-deep > .v-tabs-bar {
  background-color: #fafafa;
  border-bottom: 1px solid #e0e0e0;
}

.list-wrapper {
  display: flex;
  // justify-content: space-between;
  flex-wrap: wrap;
  // width: 90%;
  margin: 0 auto;
  background-color: white;
}
.item {
  width: 24%;
  font-size: 13px;
  list-style: disc;
  width: 210px;
  color: #3d4c4a;
  font-weight: 600;
}
.consultation-wrapper,
.staff-wrapper {
  display: flex;
  justify-content: end;
  background-color: #fafafa;
  margin-bottom: 30px;
}
.new-consultation,
.new-staff {
  background-color: #799794;
  width: 12rem;
  border-radius: 4px;
  font-size: 14px;
  font-weight: 400;
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px 0;
}

.v-card > *:last-child:not(.v-btn):not(.v-chip):not(.v-avatar) {
  background-color: #fafafa;
  padding: 0 0 20px 0;
}
.v-expansion-panel-content__wrap {
  border-top: 10px solid red;
}

.v-sheet.v-card[data-v-a04987ec]:not(.v-sheet--outlined) {
  background-color: #fafafa;
}
.input-field {
  width: 42%;
}

.base-wrapper {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 20px 60px;
  background-color: #fff;
  margin-top: 25px;
  border: 1px solid #e0e0e0;
  border-radius: 4px;
}
.card-container {
  width: 80%;
}
a {
  text-decoration: none;
}
.finance {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.gen-receipt {
  background-color: #799794;
  width: 12rem;
  border-radius: 4px;
  font-size: 14px;
  font-weight: 400;
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px 0;
  align-self: flex-end;
}
.receipt-history {
  font-size: 12px;
  color: #292929;
  font-weight: 600;
}
.v-application p {
  margin-bottom: 0;
}
.hmo-heading {
  background-color: #fff;
}
</style>
