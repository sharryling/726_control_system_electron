<template>
  <div id="wrapper">
    <div class="title">分布式光纤声波传感器自适应控制系统</div>
    <div class="mainBoxTitle">
      <div class="leftBox">输入参数</div>
      <div class="rightBox">输出参数</div>
    </div>
    <div class="mainBox">
          <div class="leftBox">
            <div class="inPutparam">频率：</div>
          <div class="inputValue">
          <a-input suffix="kHz" :value="frequency"/>
        </div>
      </div>
      <div class="rightBox">
        <div class="outPutparam">测试距离：</div>
        <input class="outputValue" value="10km"/>
      </div>
    </div>
    <div class="mainBox">
          <div class="leftBox">
            <div class="inPutparam">周期：</div>
          <div class="inputValue">
          <a-input suffix="μs"/>
        </div>
      </div>
      <div class="rightBox">
        <div class="outPutparam">空间分辨率：</div>
          <input  class="outputValue"  value="10"/>
      </div>
    </div>

    <div class="mainBox">
          <div class="leftBox">
            <div class="inPutparam">脉宽：</div>
          <div class="inputValue">
          <a-input suffix="ns"/>
        </div>
      </div>
      <div class="rightBox">
        <div class="outPutparam">灵敏度：</div>
          <input  class="outputValue" />
      </div>
    </div>

    <div class="mainBox">
          <div class="leftBox">
            <div class="inPutparam">幅值：</div>
          <div class="inputValue">
          <a-input suffix="V"/>
        </div>
      </div>
      <div class="rightBox">
        <div class="outPutparam">输出功率：</div>
          <input  class="outputValue"/>
      </div>
    </div>

    <div class="mainBox">
          <div class="leftBox">
            <div class="inPutparam">阻抗匹配：</div>
          <div class="inputValue">
          <a-input suffix="Ω"/>
        </div>
      </div>
      <div class="rightBox">
        <div class="outPutparam">信噪比：</div>
          <input  class="outputValue"/>
      </div>
    </div> 

    <div class="mainBox">
          <div class="leftBox">
      </div>
      <div class="rightBox">
        <div class="outPutparam">相关系数:</div>
          <input  class="outputValue"/>
      </div>
    </div> 
  </div>
</template>

<script>
  import SystemInformation from './LandingPage/SystemInformation'

  export default {
    name: 'landing-page',
    components: { SystemInformation },
    data () {
      return {
        frequency: 10
      }
    },
    methods: {
      open (link) {
        require('electron').shell.openExternal(link)
      }
    }
  }
</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body { font-family: 'Source Sans Pro', sans-serif; }
  #wrapper {
    background:
      radial-gradient(
        ellipse at top left,
        rgba(255, 255, 255, 1) 40%,
        rgba(229, 229, 229, .9) 100%
      );
    height: 100vh;
    padding: 30px 80px 60px 80px;
    width: 100vw;
  }
  .disabled_sytle {
    color: rgba(0, 0, 0, 0.25); background-color: #f5f5f5;
  }
  .title {
    text-align: center;
    font-weight:bold;
    font-size: 30px;
    color: #000000;
    margin-bottom: 35px;
  }
  .mainBoxTitle {
    font-weight:bold;
    font-size: 15px;
    margin:5px;
  }
  .mainBox, .mainBoxTitle {
    display:flex;
    justify-content: space-around;
    margin: 10px 0;
  }
  .leftBox {
    width: 200px;
  }
  .inPutparam, .inputValue {
    display: inline-block;
    margin: 0, 10px;
  }
  .inPutparam {
    width: 70px;
    text-align: right;
  }
  .inputValue {
    width: 75px;
  }
  .outPutparam {
    display: inline-block;
    margin: 0, 10px;
     width: 85px;
    text-align: right;
  }
  .outputValue {
    width: 75px;
    border: none;
    background: transparent;
    border-bottom: 1px solid #ccc; text-align: center;
  }
.ant-input-affix-wrapper .ant-input:not(:last-child) {
    padding-right: 35px !important;
}
</style>
