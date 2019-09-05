<template>
  <div class="SearchBar">
    <ul class="nav-btn">
      <li class="list-hover">
        <router-link to="/">我的美团</router-link>
        <dl>
          <dd>
            <router-link to="/">我的订单</router-link>
          </dd>
          <dd>
            <router-link to="/">我的收藏</router-link>
          </dd>
          <dd>
            <router-link to="/">抵用劵</router-link>
          </dd>
          <dd>
            <router-link to="/">账户设置</router-link>
          </dd>
        </dl>
      </li>
      <li>
        <router-link to="/">手机APP</router-link>
      </li>
      <li class="list-hover">
        <router-link to="/">卖家中心</router-link>
        <dl>
          <dd>
            <router-link to="/">登录商家中心</router-link>
          </dd>
          <dd>
            <router-link to="/">美团智能收银</router-link>
          </dd>
          <dd>
            <router-link to="/">我想合作</router-link>
          </dd>
          <dd>
            <router-link to="/">手机免费开店</router-link>
          </dd>
          <dd>
            <router-link to="/">餐饮代理商招募</router-link>
          </dd>
          <dd>
            <router-link to="/">商家申请开票</router-link>
          </dd>
          <dd>
            <router-link to="/">免费合作美团排队</router-link>
          </dd>
        </dl>
      </li>
      <li class="list-hover">
        <router-link to="/">网站导航</router-link>
        <div class="site-navigation">
          <dl class="box-travel">
            <dt>酒店旅游</dt>
            <dd>国际机票</dd>
            <dd>火车票</dd>
            <dd>榛果民宿</dd>
            <dd>经济型酒店</dd>
            <dd>主题酒店</dd>
            <dd>商务酒店</dd>
            <dd>公寓</dd>
            <dd>豪华酒店</dd>
            <dd>客栈</dd>
            <dd>青年旅社</dd>
            <dd>度假酒店</dd>
            <dd>别墅</dd>
            <dd>农家院</dd>
          </dl>
          <dl class="box-gourmet">
            <dt>吃美食</dt>
            <dd>烤鱼</dd>
            <dd>特色小吃</dd>
            <dd>烧烤</dd>
            <dd>自助餐</dd>
            <dd>火锅</dd>
            <dd>代金劵</dd>
          </dl>
          <dl class="box-movies">
            <dt>看电影</dt>
            <dd>热映电影</dd>
            <dd>热门影院</dd>
            <dd>热映电影口碑榜</dd>
            <dd>最受期待电影</dd>
            <dd>国内票房榜</dd>
            <dd>北美票房榜</dd>
            <dd>电影排行榜</dd>
          </dl>
          <dl class="box-app">
            <dt>手机应用</dt>
            <dd>
              <img src="//s0.meituan.net/bs/fe-web-meituan/2d53095/img/appicons/meituan.png" />
              <img src="//s1.meituan.net/bs/fe-web-meituan/404d350/img/appicons/waimai.png" />
              <img src="//s0.meituan.net/bs/fe-web-meituan/404d350/img/appicons/zhenguo.png" />
              <img src="//s1.meituan.net/bs/fe-web-meituan/404d350/img/appicons/dianping.png" />
              <img src="//s1.meituan.net/bs/fe-web-meituan/404d350/img/appicons/maoyan.png" />
            </dd>
          </dl>
        </div>
      </li>
    </ul>
  </div>
</template>


<style lang="less">
.SearchBar {
  display: inline-block;

  ul.nav-btn > li {
    display: inline-block;
    padding: 12px 14px;
    line-height: 16px;
    text-align: center;
    position: relative;
  }
  ul.nav-btn > li > dl {
        z-index: 1;
    position: absolute;
    top: 40px;
    right: 0;
    display: none;
    background: #fff;
    box-shadow: 0 0 2px rgba(102, 102, 102, 0.3);
  }
  ul.nav-btn > li > dl > dd {
    text-align: center;
    white-space: nowrap;
    line-height: 35px;
    min-width: 75px;
    padding: 0 10px;
  }
  ul.nav-btn > li > div.site-navigation {
    z-index: 5;
    position: absolute;
    top: 40px;
    right: 0;
    max-width: 1190px;
    width: 1190px;
    height: 295px;
    padding: 30px 36px 36px 47px;
    background: #fff;
    box-shadow: 0 0 2px rgba(102, 102, 102, 0.3);
    text-align: left;
    display: none;

    dl {
      color: #666;
      vertical-align: top;
      width: 240px;
      margin-right: 40px;
      float: left;

      dt {
        width: 100%;
        font-weight: 600;
        font-size: 16px;
        text-align: center;
        margin-bottom: 36px;
        cursor: default;
      }
      dd {
        text-align: center;
        line-height: 26px;
        width: 33.333%;
        flex-grow: 1;
        float: left;
        cursor: pointer;
      }
      dd:hover {
        color: #fe8c00;
      }
    }
    .box-travel {
    }
    .box-gourmet {
      width: 156px;
      dd {
        width: 50%;
      }
    }
    .box-movies {
      width: 90px;
      dd {
        width: 100%;
      }
    }
    .box-app {
      width: 380px;
      dd {
        font-size: 0;
        display: block;
        width: 100%;
        height: 60px;
        cursor: default;
        img{
          width: 60px;
          height: 60px;
          margin: 0 7px;
          cursor: pointer;
        }
      }
    }
  }

  // --------------------------------------------
  ul.nav-btn > li.list-hover:hover {
    box-shadow: 0 -2px 2px rgba(102, 102, 102, 0.3);
    background: #fff;
  }
  ul.nav-btn > li.list-hover:hover > dl {
    display: block;
  }
  ul.nav-btn > li.list-hover:hover > div.site-navigation {
    display: block;
  }
}
</style>