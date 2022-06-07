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
      <img :src="item.action" class="h-5" alt="hamburger">
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
            text: 'I.D',
            align: 'left',
            sortable: false,
            value: 'number',
          },
          { text: 'Name', value: 'name', align:'left'},
          { text: 'Email Address', value: 'email',  align:'left' },
          { text: 'Gender', value: 'gender',  align:'left' },
          { text: 'Age', value: 'age',  align:'left' },
          { text: 'Time Queued', value: 'time', align:'left' },
          { text: '', value: 'action',  align:'left'  }
        ],
        tableDetails: [
          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            gender: 'Male',
            age: 49,
            time: '11:59AM',
            action: '/three-dots.png'
          },
          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            gender: 'Male',
            age: 49,
            time: '11:59AM',
            action: '/three-dots.png'

          },
          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            gender: 'Male',
            age: 49,
            time: '11:59AM',
            action: '/three-dots.png'

          },
          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            gender: 'Male',
            age: 49,
            time: '11:59AM',
            action: '/three-dots.png'

          },
          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            gender: 'Male',
            age: 49,
            time: '11:59AM',
            action: '/three-dots.png'

          },
          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            gender: 'Male',
            age: 49,
            time: '11:59AM',
            action: '/three-dots.png'

          },
          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            gender: 'Male',
            age: 49,
            time: '11:59AM',
            action: '/three-dots.png'

          },
          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            gender: 'Male',
            age: 49,
            time: '11:59AM',
            action: '/three-dots.png'

          },
          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            gender: 'Male',
            age: 49,
            time: '11:59AM',
            action: '/three-dots.png'

          },
          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            gender: 'Male',
            age: 49,
            time: '11:59AM',
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