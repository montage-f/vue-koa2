/**Created by MonTage_fz on 2019/3/30**/
<template>
  <div class="Login-register">
    <div class="position">
      <span class="city">北京</span>
      <a href="###" class="change-city">切换城市</a>
      <div class="city-position">
        [
        <a href="###">大厂回族自治县</a>
        <a href="###">香河</a>
        <a href="###">玉田县</a>
        ]
      </div>
      <div class="login-register">
        <a href="###" class="login">立即登录</a>
        <a href="/register" class="register">注册</a>
      </div>
    </div>
    <div class="nav">
      <ul class="bar">
        <li class="in-select">
          <a href="###">我的美团</a>
          <ul class="select-my-mt">
            <li>
              <a href="###">我的订单</a>
            </li>
            <li>
              <a href="###">我的收藏</a>
            </li>
            <li>
              <a href="###">抵用券</a>
            </li>
            <li>
              <a href="###">账户设置</a>
            </li>
          </ul>
        </li>
        <li>
          <a href="###">手机App</a>
        </li>
        <li class="in-select">
          <a href="###">商家中心</a>
          <ul class="select-business-center">
            <li>
              <a href="###">登录商家中心</a>
            </li>
            <li>
              <a href="###">美团智能收银</a>
            </li>
            <li>
              <a href="###">我想合作</a>
            </li>
            <li>
              <a href="###">手机免费开店</a>
            </li>
            <li>
              <a href="###">餐饮代理商招募</a>
            </li>
            <li>
              <a href="###">商家申请开票</a>
            </li>
            <li>
              <a href="###">免费合作美团排队</a>
            </li>
          </ul>
        </li>
        <li class="in-select">
          <a href="###">网站导航</a>
          <div class="net-bar">
            <div class="select">
              <dl class="travel">
                <dt>
                  酒店旅游
                </dt>
                <dd>
                  <a href="###">国际机票</a>
                </dd>
                <dd>
                  <a href="###">火车票</a>
                </dd>
                <dd>
                  <a href="###">棒果民宿</a>
                </dd>
                <dd>
                  <a href="###">经济型酒店</a>
                </dd>
                <dd>
                  <a href="###">主题酒店</a>
                </dd>
                <dd>
                  <a href="###">商务酒店</a>
                </dd>
                <dd>
                  <a href="###">公寓</a>
                </dd>
                <dd>
                  <a href="###">豪华酒店</a>
                </dd>
                <dd>
                  <a href="###">客栈</a>
                </dd>
                <dd>
                  <a href="###">青年旅社</a>
                </dd>
                <dd>
                  <a href="###">度假酒店</a>
                </dd>
                <dd>
                  <a href="###">别墅</a>
                </dd>
                <dd>
                  <a href="###">农家院</a>
                </dd>
              </dl>
              <dl class="food">
                <dt>
                  吃美食
                </dt>
                <dd>
                  <a href="###">烤鱼</a>
                </dd>
                <dd>
                  <a href="###">烧烤</a>
                </dd>
                <dd>
                  <a href="###">火锅</a>
                </dd>
                <dd>
                  <a href="###">特色小吃</a>
                </dd>
                <dd>
                  <a href="###">自助餐</a>
                </dd>
                <dd>
                  <a href="###">代金券</a>
                </dd>
              </dl>
              <dl class="movie">
                <dt>
                  看电影
                </dt>
                <dd>
                  <a href="###">热门电影</a>
                </dd>
                <dd>
                  <a href="###">热门影院</a>
                </dd>
                <dd>
                  <a href="###">热映电影口碑榜</a>
                </dd>
                <dd>
                  <a href="###">最受期待电影</a>
                </dd>
                <dd>
                  <a href="###">国内票房榜</a>
                </dd>
                <dd>
                  <a href="###">北美票房榜</a>
                </dd>
                <dd>
                  <a href="###">电影排行榜</a>
                </dd>
              </dl>
              <dl class="phone">
                <dt>手机应用</dt>
                <dd></dd>
              </dl>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Login-register',
    components: {},
    data() {
      return {}
    },
    created() {
    },
    mounted() {
    },
    computed: {},
    methods: {}
  }
</script>

<style scoped lang="less">
  .Login-register {
    margin: 0 auto;
    height: 40px;
    max-width: 1190px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    a:hover {
      color: #31bbac;
    }
    .position {
      display: flex;
      .city {
        margin-right: 4px;
      }
      .change-city {
        background: #F4F4F4;
        border: 1px solid #E5E5E5;
        color: #666;
        border-radius: 2px;
        margin: 0 4px;
        padding: 0 2px;
        &:hover {
          color: #31bbac;
        }
      }
      .city-position {
        margin-right: 26px;

      }
      .login-register {
        .login {
          color: #31bbac;
          margin-right: 9px;
        }
      }
    }
    .nav {
      .bar {
        display: flex;
        > li {
          padding: 12px 14px;
          position: relative;
          box-sizing: border-box;
          a {
            display: inline-block;
            height: 100%;
          }
          &.in-select {
            &:hover {
              background: #fff;
              box-shadow: 0 3px 5px 0 rgba(0, 0, 0, .1);
              & > ul {
                display: block;
              }
              .net-bar {
                display: block;
                border: 1px solid #fff;
              }
            }
            > ul {
              display: none;
              position: absolute;
              background: #fff;
              text-align: center;
              z-index: 1000;
              border-top: 0;
              top: 40px;
              padding: 12px 0;
              box-shadow: 0 3px 5px 0 rgba(0, 0, 0, .1);
              li {
                padding-top: 12px;
                &:nth-of-type(1) {
                  padding-top: 0;
                }
              }
            }
            .net-bar {
              display: none;
              background: #fff;
              position: absolute;
              z-index: 1000;
              right: 0;
              top: 40px;
              width: 1200px;
              box-sizing: border-box;
              border-top-left-radius: 4px;
              padding: 30px 36px 36px 47px;
              border: 1px solid #E5E5E5;
              box-shadow: 0 3px 5px 0 rgba(0, 0, 0, .1);
              .select {
                display: flex;
                font-size: 12px;
                text-align: center;
                dt {
                  font-size: 14px;
                  width: 100%;
                  margin-bottom: 36px;
                  color: #31bbac;
                }
                dd {
                  color: #999999;
                }
                .travel {
                  width: 253px;
                  dd {
                    float: left;
                    margin: 7px 12px 0 0;
                    width: 70px;
                  }
                }
                .food {
                  width: 193px;
                  dd {
                    margin: 7px 8px 0;
                    float: left;
                    width: 80px;
                  }
                }
                .movie {
                  width: 162px;
                  dd {
                    margin-top: 7px;
                    float: left;
                    width: 100%;
                  }
                }
                .phone {
                  flex: 1;
                }
              }
            }
            .select-my-mt {
              width: 100%;
              left: 0;
            }
            .select-business-center {
              width: 140%;
              right: 0;

            }
          }
        }

      }
    }
  }
</style>
