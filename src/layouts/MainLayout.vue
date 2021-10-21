<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container>
      <ContainerHeader/>
      <router-view />
      <!-- <Footer/> -->
      
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import ContainerHeader from 'src/components/common/ContainerHeader.vue'
import Footer from 'src/components/common/Footer.vue'
import { defineComponent,  } from 'vue'

export default defineComponent({
  name: 'MainLayout',
  components: {
    ContainerHeader
    
    
  },
})
</script>
