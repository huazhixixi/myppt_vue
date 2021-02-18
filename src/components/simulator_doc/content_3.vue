<template>
  <section>
    <navbar section_title="The tranciever package"></navbar>

  <div class="container-fluid">
    <div class="row h-100 shadow">
      <div class="col-6">
        <span class="section_body  text-justify d-inline-block"> tranciever 主要实现了收发端DSP 和器件损伤的建模，
          分别在dsp.py 中和instruments.py中实现，主要功能如下
        </span>

        <br/>
        <br/>

        <span class="font-weight-bold section_body d-inline-block text-left w-100">器件建模</span>
        <span class="section_body d-inline-block text-left w-100" style="padding-left: 2em">
            <strong>instruments.py 中的函数：</strong>
            <br/>
            1. Laser(power_dbm, lw , fo):power_dbm: 激光器功率，lw：线宽，fo:频偏
            <br/>
            2. ADC
            <br/>
            3. DAC
        </span>

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

      <div class="col-6">

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
