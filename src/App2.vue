<template>
  <div id="app">
    <!--pc nav-->
    <section class="nav-bar">
      <div class="nav-container">
        <div class="brand"><img src="./assets/img/logo2.png" width="300" height="80"></div>
        <ul>
          <router-link tag="li" to="/home" >首页</router-link>
          <router-link tag="li" to="/study">编程学习</router-link>
          <router-link tag="li" to="/home">兴趣爱好</router-link>
          <router-link tag="li" to="/home">关于我</router-link>
          <router-link tag="li" to="/home">留言板</router-link>
        </ul>
        <div class="login-regist">
          <a href="#">登录</a> / <a href="#">注册</a>
        </div>
      </div>


    </section>

    <!--app nav-->
    <section class="app-nav-bar clearfloat">
      <div class="btn-bar">
        <i class="icon iconfont icon-menu"></i>
      </div>
      <div class="title">Charles个人博客</div>
      <a href="#" class="me"><img src="http://jspang.com/static//myimg/blogtouxiang.jpg" alt=""></a>
    </section>

    <!--侧边栏-->
    <aside class="app-aside">
      <div class="aside-box">aside-box</div>
    </aside>


    <!--内容-->
    <section class="content-container clearfloat">
      <section class="main">
        <router-view/>
      </section>
      <aside class="aside">

      </aside>

    </section>


  </div>
</template>

<script>
  import '@/assets/css/reset.css'
  import '@/assets/css/utils.css'

  export default {
    name: 'App'
  }
</script>

<style scoped lang="scss">
  $maincolor: #b5644c;
  $secondecolor: #e0ba96;
  .nav-bar {
    background: #ffffff;
    font-size: 14px;
    color: #333;
    -webkit-box-shadow: 2px 0 6px rgba(133, 100, 76, 0.5);
    box-shadow: 2px 0 6px rgba(133, 100, 76, 0.5);
    margin-bottom: 10px;
    position: fixed;
    width: 100%;
    height: 80px;
    .nav-container {
      margin: 0 auto;
      width: 1200px;
      height: 80px;
      line-height: 80px;
      .brand {
        float: left;
      }
      li {
        list-style: none;
        padding: 0 25px;
        float: left;
        text-align: center;
        &:hover {
          color: $maincolor;
          cursor: pointer;
        }
      }
      .login-regist {
        float: right;
        a {
          color: #333;
          &:hover {
            color: $maincolor;
          }
        }
      }
    }
  }

  .app-nav-bar {
    display: none;
  }

  .app-aside {
    display: none;
  }

  .content-container {
    padding: 90px 3px;
    margin: 0 auto ;
    max-width: 1200px;
    height: 100%;
    position: relative;
    color: #333;
    z-index: -1;
    .main {
      min-width: 780px;
      margin-right: 290px;
      background: #ffffff;
      height: 100%;
      padding:0 24px ;
    }
    .aside {
      position: absolute;
      top: 90px;
      right: 0;
      width: 280px;
      background: #ffffff;
      height: 100%;
    }
  }

  @media screen and (max-width: 768px) {
    body, html {
      width: 100%;
      height: 100%;
    }
    #app {
      width: 100%;
      height: 100%;
    }
    .nav-bar {
      display: none;
    }

    .aside{
      display: none;
    }
    .app-nav-bar {
      width: 100%;
      background: #323436;
      height: 50px;
      color: #e5e5e5;
      display: block;
      line-height: 50px;
      position: fixed;
      top: 0;
      left: 0;
      .btn-bar {
        position: absolute;
        left: 5px;
      }
      .title {
        text-align: center;
        font-size: 14px;
      }
      .me {
        position: absolute;
        right: 10px;
        top: 10px;
        img {
          width: 30px;
          height: 30px;
          border-radius: 30px;
          overflow: hidden;
        }
      }
    }

    .content-container {
      margin-top: 50px;

    }

    /*侧边栏*/
    .app-aside {
      display: none;
      height: 100%;
      background: rgba(0, 0, 0, 0.5);
      color: #f1f1f1;
      /*display: block;*/
      z-index: 999;
      position: fixed;
      width: 100%;
      top: 0;
      left: 0;
      overflow: hidden;
      .aside-box {
        padding-top: 50px;
        width: 200px;
        background: #4A4A4A;
        color: #f1f1f1;
        height: 100%;
      }
    }

  }


</style>
