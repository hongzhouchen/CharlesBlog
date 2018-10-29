<template>
    <section class="row">
       <div class="article-item clearfloat">

         <div class="col-xs-12 col-lg-4 app-mb10">
             <img :src="articledata.article_banner" alt="" width="100%">
         </div>

         <div class="col-xs-12 col-lg-8">
           <div class="article-item-content-box">
             <div class="article-item-title"> {{articledata.article_title}} </div>
             <div class="author-article-info">

               <span>作者：{{articledata.author}}</span>
               <span>分类:&nbsp;{{articledata.type}}</span>
               <span>时间：{{articledata.createtime}}</span>
              <!-- <span>阅读量：&nbsp;{{articledata.article_amount_of_access}}</span>-->
             </div>
             <div class="article-content">
               {{articledata.article_content}}
             </div>
             <a href="#" class="fr lookall">阅读全文</a>
             <a href="#" class="fl bq"><i class="iconfont  icon-biaoqian"></i>标签：&nbsp;{{articledata.article_tag}}</a>
           </div>
         </div>
       </div>
    </section>

</template>


<style lang="scss" scoped>

  .article-item {
    padding-bottom: 13px;
    margin-bottom: 10px;
    border-bottom: 1px solid #e0ba96;
    font-size: 14px;
    color: #526163;
    width: 100%;
    &:hover{
      -moz-box-shadow:10px 10px 10px #A1A1A1;
      -webkit-box-shadow:10px 10px 10px #A1A1A1;
      box-shadow:10px 10px 10px #A1A1A1;
    }

    .article-item-content-box {
      .article-item-title {
        font-size: 16px;
        font-weight: 600;
        margin-bottom: 15px;
        color: #333;
      }
      .author-article-info {
        padding: 0 0 10px 0;
        color: #b2b2b2;
        font-size: 14px;
        span {
          padding-right:30px;
        }
      }
      .article-content {
        height: 70px;
        line-height:25px;
        overflow:hidden;
        text-overflow: ellipsis;
        display: -webkit-box;
        -webkit-line-clamp: 3;
        -webkit-box-orient: vertical;
        word-break: break-all;

      }
      .lookall{
        color: #e0ba96;
        display: block;
        margin-top: 15px;
        border: 1px solid #e0ba96;
        padding: 3px 10px;
        border-radius: 50px;
        font-size: 12px;
      }
      .bq{
        color: #e0ba96;
        display: block;
        margin-top: 10px;
        padding: 5px 0;
        font-size: 12px;
      }
    }

    @media screen and (max-width: 950px) {
      .app-mb10{
        margin-bottom: 20px;
      }
    }

  }


</style>


<script>
    export default {
      props:["articledata"],
        data() {
            return {

            }
        },
      mounted:function () {

      }
    }
</script>
