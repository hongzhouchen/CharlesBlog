<template>

  <section class="row">
    <div class="col-lg-9 col-xs-12  clearfloat">
       <div class="main">
          <ArticleItem v-for="item in articleList" :articledata=item></ArticleItem>
       </div>

    </div>
    <div class="col-lg-3 col-xs-12  clearfloat">
      <div class="aside">
         <div class="aside-item">
            <header>关于我</header>
         </div>

      </div>
    </div>

  </section>

</template>

<script>

  import ArticleItem from '@/components/ArticleItem'

  export default {
    data() {
      return {
        articleList: [
          {
            id: 1,
            type: '编程技术',
            createtime: '2018/10/26',
            author: 'Charles',
            article_tag: 'Vue，编程技术，Charles',
            article_title: 'Vue 基础学习',
            article_content: 'Vue (读音 /vjuː/，类似于 view) 是一套用于构建用户界面的渐进式框架。与其它大型框架不同的是，Vue 被设计为可以自底向上逐层应用。Vue 的核心库只关注视图层，不仅易于上手，还便于与第三方库或既有项目整合。另一方面，当与现代化的工具链以及各种支持类库结合使用时，Vue 也完全能够为复杂的单页应用提供驱动。',
            article_icon: '',
            article_banner: 'http://img.zcool.cn/community/0181845834f4eda8012060c8c95113.JPG@1280w_1l_2o_100sh.png',
            article_amount_of_access: '200'
          },
          {
            id: 2,
            type: '编程技术',
            createtime: '2018/10/26',
            author: 'Charles',
            article_tag: 'Vue',
            article_title: 'Vue 基础学习',
            article_content: 'Vue (读音 /vjuː/，类似于 view) 是一套用于构建用户界面的渐进式框架。与其它大型框架不同的是，Vue 被设计为可以自底向上逐层应用。Vue 的核心库只关注视图层，不仅易于上手，还便于与第三方库或既有项目整合。另一方面，当与现代化的工具链以及各种支持类库结合使用时，Vue 也完全能够为复杂的单页应用提供驱动。',
            article_icon: '',
            article_banner: 'http://img1.imgtn.bdimg.com/it/u=667598029,2165827944&fm=26&gp=0.jpg',
            article_amount_of_access: '200'
          },
          {
            id: 3,
            type: '编程技术',
            createtime: '2018/10/26',
            author: 'Charles',
            article_tag: 'Vue',
            article_title: 'Vue 基础学习',
            article_content: 'Vue (读音 /vjuː/，类似于 view) 是一套用于构建用户界面的渐进式框架。与其它大型框架不同的是，Vue 被设计为可以自底向上逐层应用。Vue 的核心库只关注视图层，不仅易于上手，还便于与第三方库或既有项目整合。另一方面，当与现代化的工具链以及各种支持类库结合使用时，Vue 也完全能够为复杂的单页应用提供驱动。',
            article_icon: '',
            article_banner: 'http://img5.imgtn.bdimg.com/it/u=1848940053,2929103916&fm=200&gp=0.jpg',
            article_amount_of_access: '200'
          },
          {
            id: 4,
            type: '编程技术',
            createtime: '2018/10/26',
            author: 'Charles',
            article_tag: 'Vue',
            article_title: 'Vue 基础学习',
            article_content: 'Vue (读音 /vjuː/，类似于 view) 是一套用于构建用户界面的渐进式框架。与其它大型框架不同的是，Vue 被设计为可以自底向上逐层应用。Vue 的核心库只关注视图层，不仅易于上手，还便于与第三方库或既有项目整合。另一方面，当与现代化的工具链以及各种支持类库结合使用时，Vue 也完全能够为复杂的单页应用提供驱动。',
            article_icon: '',
            article_banner: 'http://img5.imgtn.bdimg.com/it/u=1148062940,3310983637&fm=200&gp=0.jpg',
            article_amount_of_access: '200'
          }
        ]
      }
    },
    components: {
      ArticleItem
    }
  }
</script>
<style lang="scss" scoped>
   .main{
    padding: 15px;
     background: #ffffff;
   }
  .aside{

    .aside-item{
      background: #ffffff;
    }
  }

</style>
