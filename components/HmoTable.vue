<template>
  <v-data-table
    v-model="selected"
    :headers="headers"
    :items="tableDetails"
    item-key="number"
    show-select
    class="elevation-1 mt-1"
    hide-default-footer

  >
  
   <template #item.action="{ item }">
      <img :src="item.action" alt="hamburger">
    </template>
  </v-data-table>

  
</template>

<script>
  export default { 

    data () {
      return {
        singleSelect: false,
        selected: [],
        headers: [
          {
            text: 'HMO Provider',
            align: 'left',
            sortable: false,
            value: 'provider',
          },
          { text: 'Patients Coverd', value: 'covered', align:'left'},
          { text: 'Pending Payment', value: 'pending',  align:'left' },
          { text: 'Toatal Amount Paid', value: 'paid',  align:'left' },
          { text: '', value: 'action',  align:'left'  }
        ],
        tableDetails: [
          {
            provider: 'Ajocard',
            covered: 50,
            pending: 'N5,000,000',
            paid: 'N400,000',
            action: '/three-dots.png'
          },
          {
            provider: 'Reliance HMO',
            covered: 29,
            pending: 'N5,000,000',
            paid: 'N400,000',
            action: '/three-dots.png'
          },
          {
            provider: 'Healthpoint HMO',
            covered: 14,
            pending: 'N5,000,000',
            paid: 'N400,000',
            action: '/three-dots.png'
          },
          {
            provider: 'Hallmark',
            covered: 43,
            pending: 'N5,000,000',
            paid: 'N400,000',
            action: '/three-dots.png'
          },
           {
            provider: 'Greenbay',
            covered: 36,
            pending: 'N5,000,000',
            paid: 'N400,000',
            action: '/three-dots.png'
          },
           {
            provider: 'Metrohealth',
            covered: 22,
            pending: 'N5,000,000',
            paid: 'N400,000',
            action: '/three-dots.png'
          },
          {
            provider: 'Total Health Trust Limited',
            covered: 43,
            pending: 'N5,000,000',
            paid: 'N400,000',
            action: '/three-dots.png'
          },
          {
            provider: 'IHMS HMO',
            covered: 11,
            pending: 'N5,000,000',
            paid: 'N400,000',
            action: '/three-dots.png'
          },
           {
            provider: 'AIICO HMO',
            covered: 27,
            pending: 'N5,000,000',
            paid: 'N400,000',
            action: '/three-dots.png'
          },
           {
            provider: 'Realcare Health Service Limited ',
            covered: 50,
            pending: 'N5,000,000',
            paid: 'N400,000',
            action: '/three-dots.png'
          },
        ],
      }
    },
  }
</script>

<style lang="scss"  scoped>

.v-data-table::v-deep th {
  background-color: #E4EAEA ;
  font-size: 13px !important;
  color: #525252;
  font-weight: 600;
}

.v-data-table::v-deep tbody tr td {
  font-size: 13px !important;
  color: #525252;
   padding: 0px 30px;

}
.v-data-table::v-deep tr:hover {
 background-color: transparent !important;
}
.theme--light.v-data-table::v-deep .v-data-table-header th.sortable .v-data-table-header__icon {
  display: none;
}

 .v-data-table >::v-deep .v-data-table__wrapper > table > tbody > tr > td,
  .v-data-table >::v-deep .v-data-table__wrapper > table > thead > tr > th {
    padding: 0 26px 0 5px;
  }

</style>