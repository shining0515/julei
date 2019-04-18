<template>
  <div class="head">
    <div>
      <p>
        <img src="../assets/images/icon-phone.png" width="22" alt="" />
        技术支撑电话：陈文葛 156-2001-1553
      </p>
      <p>
        <img src="../assets/images/icon-msg.png" width="30" alt="" />
        技术支撑邮箱：陈文葛 chenwg24@chinaunicom.cn
      </p>
    </div>
    <img src="../assets/images/title.png" width="45%" alt="" />
    <div>
      <p>
        <span>上午 09:59:59 </span>
        <span class="pointer">
          <img src="../assets/images/icon-user.png" height="14" />
          登录人：陈文葛
        </span>
        <span class="pointer">
          <img src="../assets/images/icon-logout.png" height="14" />
          退出登录
        </span>
      </p>
      <p>
        <span class="pointer">
          <img src="../assets/images/icon-file.png" height="16" />
          聚类市场基础明细下载
        </span>
        <span class="pointer">
          <img src="../assets/images/icon-file.png" height="16" />
          聚类市场基础明细下载
        </span>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "head"
};
</script>

<style lang="less" scoped>
.head {
  height: 70px;
  display: flex;
  div {
    width: 27.5%;
    padding: 0 8px;
    p {
      display: flex;
      align-items: center;
      line-height: 29px;
    }
  }
  div:nth-child(1) p:nth-child(1),
  div:nth-child(3) p {
    img:nth-child(1) {
      margin: 0 4px;
    }
  }
  div:nth-child(3) {
    p {
      justify-content: space-between;
    }
  }
}
</style>