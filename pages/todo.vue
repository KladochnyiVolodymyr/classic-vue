<template>
    <div class="container wrapper">
        <div class="todo">
            <h1 class="todo__title">TODO</h1>
            <input class="todo__new" placeholder="What needs to be done?" v-model="newTodo" @keyup.enter="addTodo">
            <ul class="todo__list" >
                <li class="task" v-for=" (todo, index) in todos" :key="index">
                    <input type="checkbox" v-model="todo.isCompleted">
                    <label class="task__title">{{todo.title}}</label>
                    <img class="task__close" src="/cross.png" v-on:click="todos.splice(index, 1);">
                </li>
                <!-- <task-todo :task-title="phone"/> -->
                <li class="task__panel">
                    <a class="is-active" href="#">All</a>
                    <a href="#">Active</a>
                    <a href="#">Completed</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
import TaskTodo from "~/components/TaskTodo.vue";
export default {
  data() {
    return {
      newTodo: "",
      todos: []
    };
  },
  components: {
    TaskTodo
  },
  methods: {
    addTodo: function() {
        this.todos.push({title:this.newTodo, isCompleted: false});
        this.newTodo = '';
    },
    removeTodo: function() {
        this.todos.splice(index, 1);
    }
  },
  computed: {
  }
};
</script>

<style lang="sass">
.todo
    padding: 50px 0px
    text-align: center
    &__title
        text-align: center
        margin-bottom: 20px
    &__new
        border: 2px solid #999
        border-radius: 10px
        width: 500px
        padding: 12px
        margin-bottom: 10px
    &__list
        width: 500px
        display: inline-block
        border: 2px solid #999
        border-radius: 10px
        padding: 10px 0px
        min-height: 200px
.task
    //width: 500px
    //border: 2px solid #999
    //border-radius: 10px
    //padding: 10px
    display: flex
    border-bottom: 1px solid #999
    padding: 10px
    display: flex
    justify-content: space-between
    &:last-child
        border-bottom: none
    &__close
        width: 20px
        height: 20px
        cursor: pointer
    &__panel
        margin-top: 20px
        a
            text-decoration: none
            margin-right: 30px
            color: #000
            &:hover
                color: red
            &.is-active
                color: red
input[type=checkbox] 
    opacity: 0
    position: absolute
    width: 20px
    height: 20px
input[type=checkbox] + label:before 
    content: "\2713"
    color: transparent
    display: inline-block
    border: 1px solid #999
    font-size: 20px
    line-height: 22px
    height: 20px
    width: 20px
    text-align: center
    vertical-align: middle
    transition: color ease .3s
    margin-right: 20px
input[type=checkbox]:checked + label:before 
    color: green
input[type=checkbox]:checked + label
    color: #d9d9d9
    text-decoration: line-through
</style>
