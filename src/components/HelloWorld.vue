<template>
    <main class="globalMain">
        <div class="center">
            <div class="logo">
                {{logo}}
            </div>
            <TabBar />
            <div class="search">
                <form>
                    <input type="text"/>
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
        logo: 'logo'
      }
    }
  }
</script>

<style>
    @import "../assets/css/main.css";
</style>