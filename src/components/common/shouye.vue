<template>

  <section id="shouye">
    <nav class="navbar bg-light p-0">
      <div class="navbar-brand d-flex align-items-center p-0 m-0">
        <img  src="figure/logo4.png" alt="" class="d-inline-block">
        <img src="figure/wenzi.png" width="200" height="43.891" alt="" class=" d-inline-block" >
      </div>

      <img src="figure/right.png" class="text-left" alt="">
    </nav>
    <card>
      <img src="figure/dibu.png" alt="" class="card-img">
      <div class="card-img-overlay">
        <span class="display-1 d-block text-capitalize text-center">{{ppt_title}}</span>
        <span class="h1 mt-5 d-block text-center">{{author_name}}</span>
        <span class="h1 mt-5 d-block text-center"> {{data}}</span>

      </div>
    </card>
  </section>


</template>

<script>
export default {
  name: 'FirstPage',
  props:["ppt_title","author_name","data"]
}
</script>
