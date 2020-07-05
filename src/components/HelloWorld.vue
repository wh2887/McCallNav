<template>
    <main class="globalMain">
        <div class="center">
            <div class="logo">
                {{logo}}
            </div>
            <div class="searchBar">
                <TabBar/>
                <form class="search" :action="formAction[0].url">
                    <div class="searchLogo">
                        <svg class="icon" aria-hidden="true">
                            <use xlink:href="#icon-baidu"></use>
                        </svg>
                    </div>
                    <input type="text" :name="formAction[0].inputName"/>
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

  export default {
    components: {TabBar},
    data() {
      return {
        logo: 'logo',
        formAction: [
          {url: 'https://baidu.com/s', inputName: 'wd'},
          {url: 'https://google.com/search', inputName: 'q'}
        ],

      }
    }
  }
</script>

<style>
    @import "../assets/css/main.css";
</style>