<template>
    <main class="globalMain">
        <ForkMe/>
        <div class="center">
            <div class="logo">
                <img src="@/assets/images/navLogo.jpg" alt="">
            </div>
            <div class="searchBar">
                <TabBar :searchEngine="searchEngine" v-on:liIndex="index = $event"/>
                <form class="search" :action="searchEngine[index].url">
                    <div class="searchLogo">
                        <svg class="icon" aria-hidden="true">
                            <use :xlink:href="searchEngine[index].logo"></use>
                        </svg>
                    </div>
                    <input type="text" :name="searchEngine[index].inputName"/>
                    <button type="submit">
                        <svg class="icon" aria-hidden="true">
                            <use xlink:href="#icon-search1"></use>
                        </svg>
                    </button>
                </form>
            </div>
        </div>
    </main>
</template>

<script>
  import TabBar from './TabBar'
  import ForkMe from './forkMeOnGitHub.vue'

  export default {
    components: {TabBar, ForkMe},
    data() {
      return {
        index: undefined,
        searchEngine: [
          {searchName: '百度', logo: '#icon-baidu', url: 'https://baidu.com/s', inputName: 'wd'},
          {searchName: '谷歌', logo: '#icon-google', url: 'https://google.com/search', inputName: 'q'},
          {searchName: '知乎', logo: '#icon-zhihu', url: 'https://www.zhihu.com/search', inputName: 'q'},
          {searchName: 'B站', logo: '#icon-bilibili', url: 'https://search.bilibili.com/all', inputName: 'keyword'},
          {searchName: '京东', logo: '#icon-jingdong', url: 'https://search.jd.com/Search', inputName: 'keyword'},
          {searchName: '淘宝', logo: '#icon-taobao', url: 'https://s.taobao.com/search', inputName: 'q'},
        ]

      }
    },
    created() {
      this.index = 0
    },
    methods: {}
  }
</script>

<style>
    @import "../assets/css/main.css";
</style>