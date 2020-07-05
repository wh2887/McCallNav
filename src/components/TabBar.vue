<template>
    <div>
        <ol class="tabUl">
            <li v-for="(searchEngine,index) in searchEngine" :key="index" @click="$emit('liIndex',index)">
                {{searchEngine.searchName}}
            </li>
        </ol>
    </div>
</template>

<script>
  export default {
    props: ['searchEngine'],
    data() {
      return {}
    },
    methods: {

    }
  }
</script>

<style>
    @import "../assets/css/tabbar.css";
</style>