<template>

  <section>

    <navbar section_title="The Basic Dir of The Simulator"></navbar>

    <div class="container-fluid">
      <div class="row h-100 align-items-center" >
        <div class="col">
          <div class="card border-info" >
            <img src="figure/simulator/tree.png" alt="" class="card-img-top">
            <div class="card-body">
              <ul class=" list-unstyled text-left section_body list-group list-group-flush">
                <li class="list-group-item">channel</li>
                <li class="list-group-item">core</li>
                <li class="list-group-item">device_manager</li>
                <li class="list-group-item">tranciever</li>

                <li class="list-group-item">utilities.py</li>
              </ul>
            </div>
            <div>
            </div>
          </div>


        </div>
        <div class="col">
          <ul class="list-unstyled section_body" style="line-height: 1.2">
            <li class="text-left">
              <span class="fragment" style="font-weight: bold">channel:</span>
              <ul class=" list-group list-group-flush ml-5 mt-2">
                <li class="list-group-item fragment" >fiber.py:定义了非线性光纤，用分布傅里叶实现</li>
                <li class="list-group-item fragment" >EDFA.py:定义了恒增益EDFA和恒功率EDFA两种类型的EDFA</li>
                <li class="list-group-item fragment">ROADM.py: 定义了WSS函数，具体原理参照附录，理论背景</li>
                <li class="list-group-item fragment">impairments.py： 定义了一些线性损伤，例如PDL，PMD,ROP等</li>
              </ul>
            </li>

            <li class="text-left">
              <span style="font-weight: bold" class="fragment">core:</span>
              <ul class="list-group list-group-flush  ml-5 mt-2">
                <li class="list-group-item fragment">Signal.py:定义了基本的信号类;基类为Signal，其余两个类QamSignal和WdmSignal都继承自基类</li>
                <li class="list-group-item fragment">constl.py:实现了Qam符号的映射</li>

              </ul>
            </li>


            <li class="text-left">
              <span class="fragment" style="font-weight: bold">device_manager:</span>

              <ul class="list-group list-group-flush fragment  ml-5 mt-2">
                <li class="list-group-item">device.py:主要实现了CUDA设备和CPU设备的自动转换，通过装饰器 device-selection 实现</li>
                <!--											<li class="list-group-item">constl.py:实现了Qam符号的映射</li>-->
              </ul>
            </li>

          </ul>
        </div>
      </div>
    </div>

  </section>

</template>

<script>
import navbar from "@/components/common/navbar";
export default {
  name: "content_1",
  components:{
    navbar
  }
}
</script>

<style scoped>

</style>
