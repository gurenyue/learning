<template>
  <div>
    <header class="site-header jumbotron">
      <div class="container">
        <div class="row">
          <div class="col-xs-12">
            <h1>请发表对React的评论</h1>
          </div>
        </div>
      </div>
    </header>
    <div class="container">
      <add :addItem="addItem"/>
      <list :comments="comments" :deleteItem="deleteItem" />

    </div>

  </div>
</template>

<script>
  import list from './list.vue';
  import add from  './add.vue';
  export default{
    components:{list,add},
    data(){
     return {
       comments : [
         {username: 'eief', content: '就那样'},
         {username: '阿斯蒂芬', content: '还可以'},
         {username: '房东是杀手', content: '什么呀'},
       ]

     }
    },
    methods:{
      addItem(comment){
        this.comments.unshift(comment);
      },
      deleteItem(index){
        this.comments.splice(index,1)
      }
    }
  }
</script>

<style>

</style>
