<template>
    <section class="real-app">
        <input 
            type="text"
            class="add-input"
            autofocus="autofocus"
            placeholder="Hey~有新任务了？"
            @keyup.enter="addTodo"
        >
        <Item :todo="todo"></Item>
    </section>
</template>

<script>
import Item from './item.vue'

export default {
    data(){
        return{
            todo:{
                id:0,
                content:'study vue.js',
                completed:false,
            },           
        }
    },
    components:{
        Item,
    },
    methods:{
        addTodo(){}
    }
}
</script>

<style lang="stylus" scoped>
.real-app{
  width 600px
  margin 0 auto
  box-shadow 0 0 5px rgba(255, 255, 255, 0.5);
}
.add-input{
  position: relative;
  margin: 0;
  width: 100%;
  font-size: 24px;
  font-family: inherit;
  font-weight: inherit;
  line-height: 1.4em;
  border: 0;
  outline: none;
  color: inherit;
  padding: 6px;
  border: 1px solid #999;
  box-shadow: inset 0 -1px 5px 0 rgba(0, 0, 0, 0.2);
  box-sizing: border-box;
  font-smoothing: antialiased;
  padding: 16px 16px 16px 60px;
  border: none;
  box-shadow: inset 0 -2px 1px rgba(0,0,0,0.03);
  background-color :#fff;
}
</style>


