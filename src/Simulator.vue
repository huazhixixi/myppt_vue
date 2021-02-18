<template>


  <div class="slides">
    <FirstPage ppt_title="A Flexible Simulator Based on CUAD and NUMBA"
               author_name="Huazhi Lun" data="2020.10.20"></FirstPage>
    <content_1></content_1>
    <content_2></content_2>
    <content_3></content_3>

  </div>



</template>

<script>
import FirstPage from './components/simulator_doc/shouye.vue'
import content_1 from "@/components/simulator_doc/content_1";
import content_2 from "@/components/simulator_doc/content_2";
import content_3 from "@/components/simulator_doc/content_3";
export default {
  name: 'simulator',
  components: {
    FirstPage,
    content_1,
    content_2,
    content_3
    // navbar
    // content1
  }
}
</script>

<style>
  .container-fluid{
    background-color: #f6f7f8;
  }
  .row{
    background-color: white;
  }
</style>



