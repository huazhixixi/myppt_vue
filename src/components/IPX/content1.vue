<template>

  <section>
    <navbar section_title="IPX"></navbar>
    <div class="container-fluid">

      <div class="row h-100 myborder">
        <div class="col section_body myborder d-flex align-items-center justify-content-center">
            <span class="myborder">123</span>
        </div>

        <div class="col myborder"></div>

      </div>

    </div>
  </section>

</template>

<script>
import navbar from "@/components/common/navbar";
export default {
  name: "content1",
  components:{
    navbar
  }
}
</script>

<style scoped>
  .myborder{
    border: 1px red solid;
  }
</style>
