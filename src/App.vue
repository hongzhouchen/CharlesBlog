<template>
  <div id="app">
    <!--pc nav-->
    <section class="nav-bar hidden-xs hidden-sm">
      <div class="container">
        <div class="row">
          <div class="brand fl"><img src="./assets/img/logo2.png" width="300" height="80"></div>
          <ul>
            <router-link tag="li" to="/home">首页</router-link>
            <router-link tag="li" to="/study">编程学习</router-link>
            <router-link tag="li" to="/">兴趣爱好</router-link>
            <router-link tag="li" to="/">关于我</router-link>
            <router-link tag="li" to="/">留言板</router-link>
          </ul>
          <div class="login-regist">
            <a href="#">登录</a> &nbsp; / &nbsp;<a href="#"> 注册</a>
          </div>
        </div>
      </div>
    </section>
    <!--app nav-->
    <section class="app-nav-bar hidden-lg hidden-md">
      <section class="container">
        <div class="row">
          <div class="col-xs-12 ">
            <div class="btn-bar">
              <i class="icon iconfont icon-menu"></i>
            </div>
            <div class="title">Charles个人博客</div>
            <a href="#" class="me"><img src="http://jspang.com/static//myimg/blogtouxiang.jpg" alt=""></a></div>
        </div>
      </section>
    </section>

    <!--content-->
    <section class="container content">
      <router-view/>

    </section>


    <footer class="footer"></footer>
  </div>
</template>

<script>
  import '@/assets/css/reset.css'
  import '@/assets/css/utils.css'

  export default {
    name: 'App'
  }
</script>

<style  lang="scss">
  $maincolor: #b5644c;
  $secondecolor: #e0ba96;
  .nav-bar{
    width: 100%;
    background: #ffffff;
    line-height: 80px;
    overflow: hidden;
    ul{
       margin-bottom: 0;
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
  .app-nav-bar {
    width: 100%;
    background: #323436;
    height: 50px;
    color: #e5e5e5;
    line-height: 50px;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 999;
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
      top: 0;
      img {
        width: 30px;
        height: 30px;
        border-radius: 30px;
        overflow: hidden;
      }
    }
  }
  .content{
    margin-top: 30px;
  }
  @media screen and (max-width: 950px) {
    .content{
      margin-top: 55px;
    }
  }







</style>
