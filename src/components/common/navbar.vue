<template>


  <nav class="navbar bg-light p-0">
    <div class="navbar-brand d-flex align-items-center p-0 m-0">
      <img  src="figure/logo4.png" alt="" class="d-inline-block">
      <img src="figure/wenzi.png" width="200" height="43.891" alt="" class=" d-inline-block" >
      <p class="d-inline-block section_biaoti">{{section_title}}</p>
    </div>

    <img src="figure/right.png" class="text-left" alt="">
  </nav>

<!--  <nav class="navbar bg-light p-0">-->
<!--    <div class="navbar-brand d-flex align-items-center p-0 m-0">-->
<!--      <img  src="figure/logo4.png" alt="" class="d-inline-block">-->
<!--      <img src="figure/wenzi.png" width="200" height="auto" alt="" class=" d-inline-block" >-->
<!--      <p class="d-inline-block section_biaoti">{{section_title}}</p>-->
<!--    </div>-->

<!--    <img src="figure/right.png" class="text-left" alt="">-->
<!--  </nav>-->
</template>

<script>
export default {
  name: "navbar",
  props:["section_title"]
}
</script>

<style scoped>

</style>
