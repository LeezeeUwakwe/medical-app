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
            text: 'Test Done',
            align: 'left',
            sortable: false,
            value: 'test',
          },
          { text: 'Date', value: 'date', align:'left'},
          { text: 'Pending Payment (Patient)', value: 'pendingPatient',  align:'left' },
          { text: 'Pending Payment (HMO)', value: 'pendingHmo',  align:'left' },
          { text: '', value: 'action',  align:'left'  }
        ],
        tableDetails: [
          {
            test: 'Malaria Test',
            date: '25th January, 2022',
            pendingPatient: 'N40,000',
            pendingHmo: 'N4,000',
            action: '/three-dots.png'
          },
           {
            test: 'HIV Test',
            date: '25th January, 2022',
            pendingPatient: 'N40,000',
            pendingHmo: 'N4,000',
            action: '/three-dots.png'
          },
          {
            test: 'Antenatal',
            date: '25th January, 2022',
            pendingPatient: 'N40,000',
            pendingHmo: 'N4,000',
            action: '/three-dots.png'
          },
          {
            test: 'Covid-19 Test',
            date: '25th January, 2022',
            pendingPatient: 'N40,000',
            pendingHmo: 'N4,000',
            action: '/three-dots.png'
          },
          {
            test: 'Daibetes Test',
            date: '25th January, 2022',
            pendingPatient: 'N40,000',
            pendingHmo: 'N4,000',
            action: '/three-dots.png'
          },
           {
            test: 'Flu (influenza) Test',
            date: '25th January, 2022',
            pendingPatient: 'N40,000',
            pendingHmo: 'N4,000',
            action: '/three-dots.png'
          },
           {
            test: 'Herpes (HSV) Test',
            date: '25th January, 2022',
            pendingPatient: 'N40,000',
            pendingHmo: 'N4,000',
            action: '/three-dots.png'
          },
          {
            test: 'Liver Function Test',
            date: '25th January, 2022',
            pendingPatient: 'N40,000',
            pendingHmo: 'N4,000',
            action: '/three-dots.png'
          },
            {
            test: 'Syphilis Test',
            date: '25th January, 2022',
            pendingPatient: 'N40,000',
            pendingHmo: 'N4,000',
            action: '/three-dots.png'
          },
           {
            test: 'Nasal Swab',
            date: '25th January, 2022',
            pendingPatient: 'N40,000',
            pendingHmo: 'N4,000',
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