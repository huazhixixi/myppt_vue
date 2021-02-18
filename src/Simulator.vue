<template>


  <div class="slides">
    <FirstPage ppt_title="A Flexible Simulator Based on CUAD and NUMBA"
               author_name="Huazhi Lun" data="2020.10.20"></FirstPage>
    <content_1></content_1>

  </div>



</template>

<script>
import FirstPage from './components/simulator_doc/shouye.vue'
import content_1 from "@/components/simulator_doc/content_1";
export default {
  name: 'simulator',
  components: {
    FirstPage,
    content_1
    // navbar
    // content1
  }
}
</script>

<style>

</style>



