<template>
  <v-data-table
    v-model="selected"
    :headers="headers"
    :items="table"
    item-key="value"
    show-select
    class="elevation-1 mt-1"
    hide-default-footer
  >
  <template #item.status="{ item }">
      <p :class="item.status === 'Online' ? 'online' : 'offline' "> {{item.status}} </p>
  </template>
  
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
            text: 'I.D',
            align: 'left',
            sortable: false,
            value: 'number',
          },
          { text: 'Name', value: 'name', align:'left' },
          { text: 'Email Address', value: 'email',  align:'left' },
          { text: 'Role', value: 'role',  align:'left'},
          { text: 'Staff Status', value: 'status', align:'left'},
          { text: '', value: 'action',  align:'left'  }
        ],
        table: [
          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            role: 'Admin',
            status: 'Online',
            action: '/three-dots.png',
            tableColor:'online'
          },
        
         {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            role: 'Super Admin',
            status: 'Online',
            action: '/three-dots.png',
            tableColor:'online'
          },
           {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            role: 'Admin',
            status: 'Offline',
            action: '/three-dots.png',
            tableColor:'offline'
          },

          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            role: 'Super Admin',
            status: 'Online',
            action: '/three-dots.png',
            tableColor:'online'
          },
          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            role: 'Super Admin',
            status: 'Offline',
            action: '/three-dots.png',
            tableColor:'offline'
          },
        {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            role: 'Admin',
            status: 'Online',
            action: '/three-dots.png',
            tableColor:'active'
          },
          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            role: 'Super Admin',
            status: 'Online',
            action: '/three-dots.png',
            tableColor:'online'
          },
          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            role: 'Super Admin',
            status: 'Offline',
            action: '/three-dots.png',
            tableColor:'offline'
          },
          {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            role: 'Super Admin',
            status: 'Online',
            action: '/three-dots.png',
            tableColor:'online'
          },
           {
            number: 142314,
            name: 'Afolabi Oluwatobiloba',
            email: 'afolabitobi200@gmail.com',
            role: 'Super Admin',
            status: 'Online',
            action: '/three-dots.png',
            tableColor:'online'
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

table .v-data-table__wrapper::v-deep > table > thead > tr > th {
    padding: 0 26px 0 5px;
}
.online {
  color: #03A300;
  background-color: #EBFFEB;
  padding: 6px 0;
  text-align: center;
  font-size: 10px;
  border-radius: 4px;
}
  .offline {
  color: #A35800;
  background-color: #FFF6EB;
  padding: 6px 0;
  text-align: center;
  font-size: 10px;
  border-radius: 4px;
  }
 .v-data-table >::v-deep .v-data-table__wrapper > table > tbody > tr > td,
  .v-data-table >::v-deep .v-data-table__wrapper > table > thead > tr > th {
    padding: 0 40px 0 5px;
  }
  .v-application p {
  margin-bottom: 0;
}
  



</style>