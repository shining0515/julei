<template>
  <div class="home">
    <j-head></j-head>
    <div class="main">
      <div class="leftDiv">
        <j-num></j-num>
        <j-income></j-income>
        <j-customer></j-customer>
      </div>
      <j-map class="midDiv"></j-map>
      <div class="rightDiv">
        <j-resource></j-resource>
        <j-develop></j-develop>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import jHead from "@/components/Head.vue";
import jNum from "@/components/Num.vue";
import jIncome from "@/components/Income.vue";
import jCustomer from "@/components/Customer.vue";
import jMap from "@/components/Map.vue";
import jResource from "@/components/Resource.vue";
import jDevelop from "@/components/Develop.vue";

export default {
  name: "home",
  components: {
    jHead,
    jNum,
    jIncome,
    jCustomer,
    jMap,
    jResource,
    jDevelop
  }
};
</script>
<style lang="less" >
.home {
  color: #2edfed;
  .pointer {
    cursor: pointer;
    display: flex;
    align-items: center;
  }
  .inner-app {
    position: relative;
  }
  .inner-main {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    > div {
      flex-grow: 1;
    }
    .inner-title {
      line-height: 2.3;
      display: flex;
      justify-content: space-between;
      padding: 7px 15px 0px 35px;
      background: url(../assets/images/icon-title.png) no-repeat 16px 60%;
      background-size: 13px;
      font-size: 13px;
      span:nth-child(1) {
        // font-weight: bolder;
      }
      span:nth-child(2) {
        color: #489fed;
      }
    }
  }
  div.main {
    padding: 0 5px;
    display: flex;
    .midDiv {
      width: 42%;
      margin: 3px;
    }
    .leftDiv,
    .rightDiv {
      width: 29%;
      flex-grow: 1;
      margin: 3px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }
  }
}
</style>


