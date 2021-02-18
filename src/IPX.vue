<template>
  <div class="slides">
    <FirstPage ppt_title="IPX" author_name="Huazhi Lun" data="2021.2.24"></FirstPage>
    <content1></content1>
  </div>
</template>

<script>
import FirstPage from "@/components/common/shouye";
import navbar from "@/components/common/navbar";
import content1 from "@/components/IPX/content1";
export default {
name: "IPX",
  components:{
  FirstPage,
    content1
  }
}
</script>

<style scoped>

</style>
