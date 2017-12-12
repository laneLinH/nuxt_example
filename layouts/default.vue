<template>
    <div>
        <header>
            <titleList :titleList="titleList"/>
        </header>
        <nuxt/>
        <footer>footer</footer>
    </div>
</template>
<script>
    import titleList from '../components/header/titleList.vue'
    export default{
        components: {
            titleList
        },
        data:function(){
          return {
              titleList: [
                  {name: '标题1', url: '/login'},
                  {name: '标题2', url: '/'},
                  {name: '标题3', url: '/'},
                  {name: '标题4', url: '/'},
                  {name: '标题5', url: '/'}
              ]
          }
        }
    }
</script>

