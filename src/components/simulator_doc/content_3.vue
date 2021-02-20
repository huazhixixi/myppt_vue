<template>
  <section>
    <navbar section_title="The tranciever package"></navbar>

  <div class="container-fluid">
    <div class="row h-100 shadow">
      <div class="col-6" style="border-right: 4px green dashed">
        <span class="section_body  text-justify d-inline-block"> tranciever 主要实现了收发端DSP 和器件损伤的建模，分别在dsp.py 中和instruments.py中实现，主要功能如下
        </span>

        <br/>
        <br/>

        <div class="fragment" data-fragment-index="1">

          <span class="font-weight-bold section_body d-inline-block text-left w-100">器件建模</span>
          <span class="section_body d-inline-block text-left w-100" style="padding-left: 2em">
              <strong>instruments.py 中的函数：</strong>
              <br/>
              <span class="fragment highlight-current-red" data-fragment-index="4"> 1. Laser(power_dbm, lw , fo):power_dbm: 激光器功率，lw：线宽，fo:频偏</span>
              <br/>
              2. ADC
              <br/>
              3. DAC
          </span>
        </div>

        <div class="fragment" data-fragment-index="2">

          <span class="font-weight-bold section_body d-inline-block text-left w-100">DSP</span>
          <span class="section_body d-inline-block text-left w-100" style="padding-left: 2em">
            <strong>dsp.py 中的函数：</strong>
            <br/>
            1. PulseShaping
            <br/>
            2. IdealResampler
            <br/>
            3. CDC
            <br/>
            4. LMS_PLL
            <br/>
            5. SuperScalaer
        </span>
        </div>



      </div>

      <div class="col-6">

        <div class="fragment" data-fragment-index="3">

          <div class="fragment highlight-current-red" data-fragment-index="4">
            <span class="section_body text-left d-inline-block w-100">The modeling of Laser Phase Noise:</span>
            <span class="section_body text-left d-inline-block w-100" style="text-indent: 2em"> 维纳过程: </span>
          </div>

        </div>


      </div>

    </div>


  </div>
  </section>
</template>

<script>
import navbar from "@/components/common/navbar";
export default {
  name: "content_3",
  components:{
    navbar
  }
}
</script>

<style scoped>

</style>
