<template>
  <section>
    <navbar section_title="Widget"></navbar>

    <div class="container-fluid">
      <div class="row h-100">
        <div class="col">
          <h1 class="section_biaoti"> Creating Widgets</h1>
          <ul class="list-group-flush list-group section_body text-left">
            DearPygui 的部件可以分为以下几个部分
            <li class="list-group-item">
              普通部件 (inputs，buttons)
            </li>
            <li class="list-group-item">容器部件（window,popup,tooltip,child）</li>
            <li class="list-group-item">布局部件 （group，next_column）</li>
            <li class="list-group-item">每个部件通过各自的add_** 或者相应的上下文管理器添加</li>
          </ul>
          <hr/>
          <span class="section_body d-inline-block text-left w-100 font-weight-bold">每个部件必须有自己独一无二的名字，默认情况下这些名字为成为部件的label，部件显示的label可以通过label关键字指定</span>
          <ul class="list-group section_body list-group-flush text-left">
            <li class="list-group-item">使用label关键字会改变部件的显示名称</li>
            <li class="list-group-item">指定name时可以使用##指定</li>
          </ul>


        </div>
      </div>
    </div>
  </section>


</template>

<script>
import navbar from "@/components/common/navbar";
export default {
  name: "get_started_01",
  components:{
    navbar
  }
}
</script>

<style scoped>

</style>
