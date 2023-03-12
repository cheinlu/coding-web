<template>
  <div class="header">
    <div class="header-container">
      <!-- 头部logo -->
      <div class="header-logo">
        <img class="img-left" src="@/assets/header-logo.png" />
        <span class="header-line"></span>
        <img class="img-right" src="@/assets/tx-logo-coding.png" />
      </div>
      <!-- item项 -->
      <ul class="header-list">
        <li class="header-list-item">
          <a href="#" class="active">首页</a>
        </li>
        <li class="header-list-item">
          <a href="#">实验室</a>
        </li>
        <li class="header-list-item">
          <a href="#">课程</a>
        </li>
        <li class="header-list-item">
          <a href="#">名师团</a>
        </li>
        <li class="header-list-item">
          <a href="#">校园</a>
        </li>
        <li class="header-list-item">
          <a href="#">社区</a>
        </li>
        <li class="header-list-item">
          <a href="#">追梦营</a>
        </li>
        <li class="header-list-item">
          <a href="#">CodingDay</a>
        </li>
        <li class="header-list-item">
          <a href="#">赛事活动</a>
        </li>
      </ul>
      <!-- 工具/登录 -->
      <div class="header-tool">
        <div class="header-select">
          <!-- 立即创作 -->
          <Dropdown style="margin-left: 20px;border-radius: 17px;">
            <Button type="primary">
              立即创作
              <Icon type="ios-arrow-down"></Icon>
            </Button>
            <DropdownMenu slot="list">
              <DropdownItem><Icon type="ios-bicycle" size="20" />创意实验室</DropdownItem>
              <DropdownItem><Icon type="ios-bicycle" size="20" />python实验室</DropdownItem>
              <DropdownItem><Icon type="ios-bicycle" size="20" />3D实验室</DropdownItem>
              <DropdownItem><Icon type="ios-bicycle" size="20" />人工智能实验室</DropdownItem>
              <DropdownItem><Icon type="ios-bicycle" size="20" />游戏实验室</DropdownItem>
              <DropdownItem><Icon type="ios-bicycle" size="20" />艺术(p5)实验室</DropdownItem>
              <DropdownItem><Icon type="ios-bicycle" size="20" />硬件实验室</DropdownItem>
              <DropdownItem><Icon type="ios-bicycle" size="20" />JS实验室</DropdownItem>
            </DropdownMenu>
          </Dropdown>
        </div>
        <div class="header-login">
          <a href="#">登录</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="less" scoped>
ul,
ol,
li {
  list-style: none;
}

.header {
  background-color: #fff;
  height: 60px;
  
  .header-container {
    height: 60px;
    position: relative;
    display: flex;
    align-items: center;
    .header-logo {
      width: 380px;
      padding-left: 40px;
      display: flex;
      align-items: center;
      position: relative;
      .img-left {
        width: 180px;
        height: 52px;
      }
      .header-line {
        width: 1px;
        height: 25px;
        background-color: #d4dce8;
        display: block;
        margin: 0 10px;
      }
      .img-right {
        width: 133px;
        height: 57px;
      }
    }
    .header-list {
      margin-left: 20px;
      display: flex;
      align-items: center;
      flex-flow: row wrap;
      .header-list-item {
        a {
          display: block;
          border-radius: 26px;
          padding: 0 15px;
          height: 34px;
          line-height: 34px;
          color: #4a596f;
          &:hover {
            background-color: #edeef0;
          }
        }
        .active {
          color: #0080ff;
          font-weight: bold;
        }
      }
    }
    .header-tool {
      position: absolute;
      right: 40px;
      top: 0;
      height: 60px;
      display: flex;
      align-items: center;
      .header-login {
        margin: 0 0 0 20px;
        line-height: 60px;
        color: rgba(74, 89, 111, 0.6);
      }
    }
  }
}
</style>
