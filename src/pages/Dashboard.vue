<template>
  <main class="q-pa-xl">
      <div class="screen text-h5">
      Dashboard
      </div>
      <div class="flex row col-12 full-width justify-between q-py-lg">
        <div class="col-4"><RawMaterial/>  </div>
        <div class="col-7"><ProductStock/>
        </div>
      </div>
     <!-- <div class="q-pa-xl "> <Footer/></div> -->
  </main>
</template>

<script>
import RawMaterial from 'src/components/Dashboard/RawMaterial.vue'
import ProductStock from 'src/components/Dashboard/ProductStock.vue'
import Footer from 'src/components/common/Footer.vue'
export default {
  components: { RawMaterial, ProductStock },
    name:'Dashboard'

}
</script>

<style>

</style>