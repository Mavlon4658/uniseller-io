<script>
import Header from '@/components/Header.vue'
export default {
    components: {
        Header,
    }
}
</script>

<template>
  <div class="wrapper">
    <Header />
    <router-view/>
  </div>
</template>

<style>
</style>
