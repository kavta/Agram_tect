<template>
  <main>
    <Dashboard/>
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Dashboard from './Dashboard.vue';

export default defineComponent({
  components: { Dashboard },
  name: 'PageIndex',
  });
</script>
