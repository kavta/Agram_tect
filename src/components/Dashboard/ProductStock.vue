<template>
  <main>
      <q-card >
          <q-card-section>
        <div class="text-h6 q-pb-md">Product Stock</div>
        <div> 
                  <q-input outlined label="Search" class="inputField" icon="search">
                     <template v-slot:append> <q-icon name="search" /> </template>
                  </q-input></div>
              <div>
                  <q-table :rows="data" :columns="columns" row-key="name"  flat>
                    <template v-slot:body="props">
                      <q-tr  :props="props">
                        <q-td :props="props.col" v-for="row in props.row" :key="row.id" class="align-right">
                          {{ row }}
                        </q-td>
                     </q-tr>
                     </template>
                 </q-table>

              </div>
          </q-card-section>
      </q-card>
  </main>
</template>

<script>
export default {
    name:'ProductStock',
      data(){
        return{
            columns: [
        {
          name: 'sn',
          required: true,
          label: 'SN',
          align: 'left',
        },

        {
          name: 'Name ',
          label: 'Name',
          field: 'Name',
          align: 'left',
          
        },
        {
          name: 'Quantity',
          label: 'Quantity ',
          field: 'Quantity',
          align: 'left',
          
        },
        { name: 'SP', align:'left', label: 'SP', field: 'SP' },
        { name: 'MP', align:'left', label: 'MP', field: 'MP' },
        { name: 'Expiry', align:'left', label: 'Expiry', field: 'Expiry' },
        
      ],
      data: [
        {
          sn:1, 
          Name: 'kati',
          Quantity: 1000,
          SP: 120,
          MP:125,
          Expiry:"2078/06/08"
        },
         {
          sn:2, 
          Name: 'kati',
          Quantity: 1000,
          SP: 120,
          MP:125,
          Expiry:"2078/06/08"
        },
      ]

            
        }
    }


}
</script>

<style>

</style>