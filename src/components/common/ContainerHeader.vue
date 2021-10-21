<template>
  <main>
    <q-header class="nav bg-primary q-px-xl q-py-sm flex justify-between items-center ">
        <div class="text-h5 text-weight-bold gt-md">
            <a href="" style="text-decoration:none " class="text-white text-body"> Dashboard</a>
                <q-btn-dropdown flat label="Product">
                    <q-list >
                        <q-item >
                            <q-item-section>
                                <q-item-label >Product</q-item-label>
                            </q-item-section>
                        </q-item>
                    </q-list>
                </q-btn-dropdown>

                <q-btn-dropdown flat label="Raw Materials">
                    <q-list>
                        <q-item>
                            <q-item-section>
                                <q-item-label>
                                    Raw Materials
                                </q-item-label>
                            </q-item-section>
                        </q-item>
                    </q-list>
                </q-btn-dropdown>

                <q-btn-dropdown flat label="Expenses">
                    <q-list>
                        <q-item>
                            <q-item-section>
                                <q-item-label>
                                    Expenses
                                </q-item-label>
                            </q-item-section>
                        </q-item>
                    </q-list>
                </q-btn-dropdown>

                <q-btn-dropdown flat label="Report">
                    <q-list>
                        <q-item>
                            <q-item-section>
                                <q-item-label>
                                    Report
                                </q-item-label>
                            </q-item-section>
                        </q-item>
                    </q-list>
                </q-btn-dropdown>

                <q-btn-dropdown flat label="Vendors/Customers">
                    <q-list>
                        <q-item>
                            <q-item-section>
                                <q-item-label>
                                Customers
                                </q-item-label>
                            </q-item-section>
                        </q-item>
                    </q-list>
                </q-btn-dropdown>

                <q-btn-dropdown flat label="Master">
                    <q-list>
                        <q-item>
                            <q-item-section>
                                <q-item-label>
                                    Master
                                </q-item-label>
                            </q-item-section>
                        </q-item>
                    </q-list>
                </q-btn-dropdown>
        </div>
         <div class="text-h5 text-weight-bold lt-md">
            <q-btn flat dense icon="menu" @click="leftDrawerOpen=!leftDrawerOpen"> 
            </q-btn>
        </div>
            <q-drawer
            v-model="leftDrawerOpen"
            class="text-primary q-py-lg"
            bordered
            >
             <a href="" style="text-decoration:none " class="text-primary text-h5 q-pa-xl"> Dashboard</a>
                     <q-list>
                        <q-item >
                            <q-item-section>
                                <q-item-label >Product</q-item-label>
                            </q-item-section>
                        </q-item>
                    </q-list>
                <q-separator/>
                    <q-list>
                        <q-item>
                            <q-item-section>
                                <q-item-label>
                                    Raw Materials
                                </q-item-label>
                            </q-item-section>
                        </q-item>
                    </q-list>
                <q-separator/>
                
                    <q-list>
                        <q-item>
                            <q-item-section>
                                <q-item-label>
                                    Expenses
                                </q-item-label>
                            </q-item-section>
                        </q-item>
                    </q-list>
                <q-separator/>
                    <q-list>
                        <q-item>
                            <q-item-section>
                                <q-item-label>
                                    Report
                                </q-item-label>
                            </q-item-section>
                        </q-item>
                    </q-list>
                <q-separator/>
                    <q-list>
                        <q-item>
                            <q-item-section>
                                <q-item-label>
                                Customers
                                </q-item-label>
                            </q-item-section>
                        </q-item>
                    </q-list>
                <q-separator/>
                    <q-list>
                        <q-item>
                            <q-item-section>
                                <q-item-label>
                                    Master
                                </q-item-label>
                            </q-item-section>
                        </q-item>
                    </q-list>
                    <q-separator/>
                
        </q-drawer>
        <div>
            
         <q-btn-dropdown
                flat
                rounded 
                >
      <template v-slot:label>
        <div class="row items-center no-wrap">
          <q-btn round flat>
                 <q-icon name="person" /> 
                    
            </q-btn>
        </div>
      </template>

      <q-list>
        <q-item clickable >
          <q-item-section>
            <q-icon name="account_circle" color="black" size="20px" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Profile</q-item-label>
          </q-item-section>
        </q-item>
         <q-item clickable>
            <q-item-section>
            <q-icon name="settings" color="black" size="20px" />
          </q-item-section>
         <q-item-section>
            <q-item-label>Setting</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable>
            <q-item-section>
            <q-icon name="logout" color="red" size="20px" />
          </q-item-section>
         <q-item-section>
            <q-item-label class="text-red q-pr-xl">Logout</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
     </q-btn-dropdown>
    </div>

</q-header>
  </main>
</template>

<script>
export default {
    name:'ContainerHeader',
    data()
    {
        return{
            leftDrawerOpen:false
        }
    }

}
</script>

<style>

</style>