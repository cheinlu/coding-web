<template>
  <div class="sidebar">
    <a href="#" class="sidebar-guide">
      <i class="icon-spr icon-spr-guide"></i>
    </a>
    <div class="sidebar-bd" ref="backtop">
      <div class="sidebar-anchor">
        <ul class="sidebar-anchor-list">
          <li class="sidebar-anchor-item active">
            <a href="#labs" class="sidebar-anchor-item-link" @click="goPrograme">
              <Icon type="logo-nodejs" size="20" />
              <span class="sidebar-anchor-item-text">实验室</span>
            </a>
          </li>
          <li class="sidebar-anchor-item active">
            <a href="#courses" class="sidebar-anchor-item-link" @click="goPrograme">
              <Icon type="logo-nodejs" size="20" />
              <span class="sidebar-anchor-item-text">---</span>
            </a>
          </li>
          <li class="sidebar-anchor-item active">
            <a href="#" class="sidebar-anchor-item-link" @click="goPrograme">
              <Icon type="logo-nodejs" size="20" />
              <span class="sidebar-anchor-item-text">---</span>
            </a>
          </li>
          <li class="sidebar-anchor-item">
            <a href="#" class="sidebar-anchor-item-link" @click="goTop">
              <Icon type="ios-share" size="20" />
              <span class="sidebar-anchor-item-text">回顶部</span>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Sidebar',
  data() {
    return {
      num: ''
    }
  },
  mounted() {
    let backtop = this.$refs.backtop

    window.addEventListener('scroll', function () {
      this.num = document.documentElement.scrollTop
      if (this.num >= 150) {
        backtop.style.display = 'block'
      } else {
        backtop.style.display = 'none'
      }
    })
  },
  methods: {
    goTop() {
      document.documentElement.scrollTop = 0
    },
    goPrograme(){
      document.documentElement.scrollTop = 200
    }
  }
}
</script>

<style lang="less" scoped>
ul,
ol,
li {
  list-style: none;
}
.sidebar {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 110px;
  position: fixed;
  bottom: 150px;
  right: -10px;
  z-index: 13;
  height: 140px;
  .sidebar-guide {
    .icon-spr {
      display: inline-block;
      background-image: url(../assets/icon.png);
    }
    .icon-spr-guide {
      background-position: 0px -279px;
      width: 102px;
      height: 136px;
    }
  }
  .sidebar-bd {
    display: none;
    .sidebar-anchor {
      visibility: visible;

      .sidebar-anchor-list {
        background-color: #fff;
        width: 60px;
        border-radius: 10px;
        border: 1px solid #efefef;

        .sidebar-anchor-item {
          height: 68px;
          border-bottom: 1px solid #eff3f8;
          display: flex;
          font-size: 12px;
          transition: all 200ms;
          &.active {
            color: #009cff;
          }
          .sidebar-anchor-item-link {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            width: 100%;
            color: rgba(74, 89, 111, 0.6);
            &:hover {
              background-color: #009cff;
              color: #fff;
            }
            .sidebaricon {
              display: block;
              margin: 0 auto 6px;
              font-size: 18px;
            }
            .sidebaricon-labs {
            }
            .sidebar-anchor-item-text {
            }
          }
        }
      }
    }
  }
}
</style>
