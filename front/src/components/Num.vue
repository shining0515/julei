<template>
  <div class="inner-app">
    <img src="../assets/images/left-top.png" width="100%" alt="" />
    <div class="inner-main">
      <ul>
        <li v-for="(item, i) in numList" :key="i">
          <img src="../assets/images/icon-num.png" width="17" alt="" />
          <div>
            <span class="num">{{ item.num }}</span>
            <span class="name">{{ item.name }}</span>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "num",
  data() {
    return {
      numList: [
        {
          num: 7560,
          name: "聚类市场数"
        },
        {
          num: 7560,
          name: "商务楼宇"
        },
        {
          num: 7560,
          name: "专业市场"
        },
        {
          num: 7560,
          name: "工业园区"
        }
      ]
    };
  }
};
</script>

<style lang="less" scoped>
.flexcc {
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.inner-main {
  ul {
    width: 100%;
    height: 100%;
    .flexcc;
    li {
      .flexcc;
      > div {
        .flexcc;
        margin-left: 3px;
        justify-content: center;
        flex-direction: column;
        line-height: 1.3;
        .num {
          font-size: 14px;
        }
        .name {
          font-size: 10px;
          color: #fff;
        }
      }
    }
  }
}
</style>