<template>
  <div>
    <header class="site-header jumbotron">
      <div class="container">
        <div class="row">
          <div class="col-xs-12">
            <h1>请发表对Vue的评论</h1>
          </div>
        </div>
      </div>
    </header>
    <div class="container">
      <Add @refresh="refresh"/>
      <List :comments="comments"/>
    </div>
  </div>
</template>

<script>
import Add from './components/add'
import List from './components/list'


export default {
  name: 'App',
  components: {
    Add,List
  },
  data(){
    return{
      comments:[
        {name:'詹姆斯.哈登',content:'我是大胡子，我是mvp'},
        {name:'克里斯.保罗',content:'我是谁？我是cp3'},
        {name:'阿伦.艾佛森',content:'我只有183，我却无人能挡'}
      ],
    }
  },
  methods:{
    refresh(name,content){
      var comment={name,content};

      this.comments.push(comment);
    },
    
  },
  // mouted(){
  //   console.log(this)
  // }
}
</script>

<style>

</style>
