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
            text: 'Name',
            align: 'left',
            sortable: false,
            value: 'drug',
          },
          { text: 'Quantity Sold', value: 'sold', align:'left'},
          { text: 'Income', value: 'income',  align:'left' },
          { text: 'Pending Payment (Patient)', value: 'pendingPatient',  align:'left' },
          { text: 'Pending Payment (HMO)', value: 'pendingHmo',  align:'left' },
          { text: '', value: 'action',  align:'left'  }
        ],
        tableDetails: [
          {
            drug: 'Paracetamol',
            sold: 50,
            income: 'N5,000,000',
            pendingPatient: 'N400,000',
            pendingHmo: 'N400,000',
            action: '/three-dots.png'
          },
          {
            drug: 'Paracetamol',
            sold: 50,
            income: 'N5,000,000',
            pendingPatient: 'N400,000',
            pendingHmo: 'N400,000',
            action: '/three-dots.png'
          },
          {
            drug: 'Paracetamol',
            sold: 50,
            income: 'N5,000,000',
            pendingPatient: 'N400,000',
            pendingHmo: 'N400,000',
            action: '/three-dots.png'
          },
          {
            drug: 'Paracetamol',
            sold: 50,
            income: 'N5,000,000',
            pendingPatient: 'N400,000',
            pendingHmo: 'N400,000',
            action: '/three-dots.png'
          },
           {
            drug: 'Paracetamol',
            sold: 50,
            income: 'N5,000,000',
            pendingPatient: 'N400,000',
            pendingHmo: 'N400,000',

            action: '/three-dots.png'
          },
           {
            drug: 'Paracetamol',
            sold: 50,
            income: 'N5,000,000',
            pendingPatient: 'N400,000',
            pendingHmo: 'N400,000',

            action: '/three-dots.png'
          },
          {
            drug: 'Paracetamol',
            sold: 50,
            income: 'N5,000,000',
            pendingPatient: 'N400,000',
            pendingHmo: 'N400,000',

            action: '/three-dots.png'
          },
          {
            drug: 'Paracetamol',
            sold: 50,
            income: 'N5,000,000',
            pendingPatient: 'N400,000',
            pendingHmo: 'N400,000',
            action: '/three-dots.png'
          },
           {
            drug: 'Paracetamol',
            sold: 50,
            income: 'N5,000,000',
            pendingPatient: 'N400,000',
            pendingHmo: 'N400,000',
            action: '/three-dots.png'
          },
           {
            drug: 'Paracetamol',
            sold: 50,
            income: 'N5,000,000',
            pendingPatient: 'N400,000',
            pendingHmo: 'N400,000',
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