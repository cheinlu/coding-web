<template>
  <div class="footer">
    <div class="footer-container">
      <!-- 底部上部分 -->
      <div class="footerList">
        <!-- logo -->
        <img class="footer-log" src="@/assets/tx-logo-coding.png" alt="" />
        <!-- 青少年编程 -->
        <div class="footer-link footer-progra">
          <p class="footer-link-title">青少年编程</p>
          <div class="footer-link-more">
            <ul class="footer-link-list">
              <li class="footer-link-item">
                <a href="#">首页</a>
              </li>
              <li class="footer-link-item">
                <a href="#">实验室</a>
              </li>
              <li class="footer-link-item">
                <a href="#">课程</a>
              </li>
              <li class="footer-link-item">
                <a href="#">名师团</a>
              </li>
              <li class="footer-link-item">
                <a href="#">校园</a>
              </li>
              <li class="footer-link-item">
                <a href="#">社区</a>
              </li>
            </ul>
            <ul class="footer-link-list">
              <li class="footer-link-item">
                <a href="#">追梦营</a>
              </li>
              <li class="footer-link-item">
                <a href="#">CodingDay</a>
              </li>
            </ul>
          </div>
        </div>
        <!-- 友情链接 -->
        <div class="footer-link footer-right">
          <p class="footer-link-title">友情链接</p>
          <div class="footer-link-more">
            <ul class="footer-link-list">
              <li class="footer-link-item">
                <a href="#">腾讯游戏追梦计划</a>
              </li>
              <li class="footer-link-item">
                <a href="#">小鹅营地</a>
              </li>
              <li class="footer-link-item">
                <a href="#">智起学堂</a>
              </li>
              <li class="footer-link-item">
                <a href="#">腾讯工蜂</a>
              </li>
            </ul>
          </div>
        </div>
        <!-- 公众号 -->
        <div class="footer-qrcode">
          <div class="footer-qrcode-img">
            <img src="@/assets/qrcode-img.jpg" alt="" />
          </div>
          <p class="footer-qrcode-text">
            关注扣叮公众号<br />
            携手创造孩子未来
          </p>
        </div>
      </div>
      <!-- 底部下部分 -->
      <div class="footer-bottom">
        <p class="copyright">Copyright © 1998 - 2023 Tencent. All Rights Reserved. 腾讯公司 版权所有</p>
        <p class="footer-bottom-link">
          <a href="#">服务协议</a>
          <span>|</span>
          <a href="#">隐私政策</a>
          <span>|</span>
          <a href="#">版权保护投诉指引</a>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="less" scoped>
.footer {
  background-color: #fff;
  padding: 35px 0;
  font-size: 14px;
  .footer-container {
    width: 1200px;
    margin: 0 auto;
    .footerList {
      display: flex;
      position: relative;
      .footer-log {
        width: 180px;
        height: 52px;
      }
      .footer-progra {
          margin: 0 40px 0 180px;
        }
      .footer-link {
       
        .footer-link-title {
          font-size: 16px;
          color: rgba(74, 89, 111, 0.6);
          margin-bottom: 12px;
        }
        .footer-link-more {
          display: flex;
          .footer-link-list {
            width: 130px;
            margin-right: 40px;
            .footer-link-item {
              line-height: 28px;
              a {
                color: #4a596f;
                text-decoration: none;
              }
              a:hover {
                color: #0080ff;
              }
            }
          }
        }
      }
      .footer-qrcode {
        right: 0;
        top: 0;
        position: absolute;
        .footer-qrcode-img {
          border: 1px solid #eff3f8;
          width: 120px;
          height: 120px;
          display: flex;
          align-items: center;
          justify-content: center;
          border-radius: 4px;
          margin-bottom: 6px;
        }
        .footer-qrcode-text {
          text-align: center;
          color: rgba(74, 89, 111, 0.6);
        }
      }
    }
    .footer-bottom {
      display: flex;
      height: 60px;
      align-items: center;
      justify-content: space-between;
      border-top: 1px solid #eff3f8;
      margin-top: 30px;

      .footer-bottom-link {
        display: flex;
        a {
          color: #4a596f;
          text-decoration: none;
        }
        a:hover {
          color: #0080ff;
        }
        span {
          color: rgba(74, 89, 111, 0.2);
          margin: 0 10px;
        }
      }
    }
  }
}
</style>
