<template>
    <ul class="header-nav">
      <li v-for="(item,index) in titleList">
          <a :class="{active:flg===index}" @click="changeNav(item,index)">{{item.name}}</a>
      </li>
    </ul>
</template>

<script>
    export default{
        props:{
            titleList:Array
        },
        data(){
            return{
                flg:0
            }
        },
        created:function(){
          console.log(1)
        },
        mounted:function(){
          console.log(2)
        },
        methods:{
            changeNav(item,index){
                this.flg=index;
                this.$router.push({path:item.url});
            }
        }
    }
</script>
