<template>

  <section>
    <navbar section_title="The core package"></navbar>

    <div class="container-fluid">
      <div class="row shadow h-100">
        <div class="col-6 d-flex flex-column">

          <span class="section_body text-left font-weight-bold">core package 中有两个文件</span>

          <ul class="list-group list-group-flush text-left section_body ">
            <li class="list-group-item section_body ">
              constl.py: 完成内部bit流到符号的映射
            </li>
            <li class="list-group-item text-justify ">
              Signal.py： 定义了基本的信号类：包括：Signal:所有信号的基类，QamSignal：单信道Qam信号和WdmSignal：波分信号
            </li>
          </ul>

          <pre class="margin_adjust">
            <code class="python text-left" data-trim>
              # 导入信号设置
              from ocsim import SignalSetting
              # 导入QamSignal
              from ocsim import QamSignal

              signal_setting = SignalSetting(
                center_freq=193.1e12,sps=2,
                device='cuda:0',symbol_rate=35e9,
                symbol_number = 65536,qam_order=16,
                need_init=True,pol_number=2
              )
              signal = QamSignal(signal_setting)
            </code>
          </pre>

        </div>

        <div class="col-6">
          <span class="section_body text-left d-inline-block">
            生成后的信号：symbol : 符号，samples 样本点，samples 存储的是升采样sps之后的结果,还需要进行如下的流程
          </span>

          <ol class="list-group list-group-flush">
            <li class="list-group-item section_body">
              1. RRC Pulseshaping: 新版的仿真采用频域实现，时域提供了一个底层函数rcosdesign
            </li>
            <li class="list-group-item section_body">
              2. Resample: 一般3 到 4 倍采样率：IdealResampler或者DAC
            </li>

            <li class="list-group-item section_body">
              3. 通过激光器，添加激光器相位噪声，频率偏移等，并设置信号的注入功率
            </li>
          </ol>
          <pre>
            <code class="python text-left" data-trim>
              from ocsim import PulseShaping
              from ocsim import Laser,IdealResampler

              shaping_filter = PulseShaping(0.02)
              laser = Laser(0,None,None) # 0dbm,lw=0,fo=0 没有相位噪声和频率偏移
              sampler = IdealResampler(old_sps = signal.sps,new_sps=4)
              signal = shaping_filter(signal)
              signal = sampler(signal)
              signal = laser(signal)

            </code>
          </pre>


        </div>
      </div>
    </div>


  </section>

</template>

<script>
import navbar from "@/components/common/navbar";
export default {
name: "content_2.vue",
  components:{
  navbar
  }
}
// alert("hello wrold");
</script>

<style scoped>

  .myborder{
    border: 1px #f6f7f8 solid;
  }

  code{
    font-size: 24px;
    line-height: 1.5em;
    overflow-scrolling: auto;
  }

  li{
    text-align: left;
  }
  li:hover{
    color: red;
  }

  .margin_adjust{
    margin-top: 6.6%;
  }
</style>
