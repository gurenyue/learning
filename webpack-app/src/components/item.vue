<template>
  <li class="list-group-item">
    <div class="handle">
      <a href="javascript:;"  @click="remove">删除</a>
    </div>
    <p class="user"><span >{{comment.username}}</span><span>说:</span></p>
    <p class="centence">{{comment.content}}</p>
  </li>
</template>

<script>
  export default{
    props:{
      comment:Object,
      index:Number,
      deleteItem:Function
  },
  methods:{
      remove(){
        const index=this.index;
        if(confirm('确定要删除此项吗？')===true){
          this.deleteItem(this.index);
        }
      }
  }
  }
</script>

<style>

</style>
