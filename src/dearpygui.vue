<template>

  <div class="slides">
    <shouye></shouye>
    <get_started_01></get_started_01>
    <get_started_02></get_started_02>
  </div>

</template>

<script>
import shouye from "@/components/dearpygui/shouye";
import get_started_01 from "@/components/dearpygui/get_started_01";
import get_started_02 from "@/components/dearpygui/get_started_02";
export default {
  name: "dearpygui",
  components:{
    shouye,
    get_started_01,
    get_started_02
  }
}
</script>

<style scoped>

</style>
