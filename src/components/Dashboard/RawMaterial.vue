<template>
  <main>
      <q-card>
          <q-card-section>
              <div class="text-h6 q-pb-md">Raw Material Stock</div>
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
    name:'RawMaterial',
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
        { name: 'Unit', align: 'left', label: 'Unit', field: 'Unit' },
        
      ],
      data: [
        {
          sn:1, 
          Name: 'BA wire 2.5"',
          Quantity: 5,
          Unit: 'KG'
        },
         {
          sn:12, 
          Name: 'C Momo',
          Quantity: 5,
          Unit: 'kG'
        },
      ]

            
        }
    }

}
</script>

<style>
.inputField {
  padding: 0px;
}

</style>