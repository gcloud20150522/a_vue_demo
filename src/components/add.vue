<template lang="html">
  <div class="col-md-4">
    <form class="form-horizontal">
      <div class="form-group">
        <label>用户名</label>
        <input type="text" class="form-control" placeholder="用户名" v-model="name">
      </div>
      <div class="form-group">
        <label>评论内容</label>
        <textarea class="form-control" rows="6" placeholder="评论内容" v-model='content'></textarea>
      </div>
      <div class="form-group">
        <div class="col-sm-offset-2 col-sm-10">
          <button type="button" class="btn btn-default pull-right" @click="add">提交</button>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
  export default {
    data(){
      return{
        name:'',
        content:''
      }
    },
    methods:{
      add(){
        this.$emit('refresh',this.name,this.content);
        console.log(this)
      }
    }
  }
</script>

<style lang="css" scoped>
</style>
