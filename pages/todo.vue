<template>
    <div class="container wrapper">
        <div class="todo">
            <h1 class="todo__title">TODO</h1>
            <input class="todo__new" placeholder="What needs to be done?" v-model="newTodo" @keyup.enter="addTodo">
            <ul class="todo__list">
                <task-todo/>
            </ul>
            <p></p>
        </div>
    </div>
</template>

<script>
import TaskTodo from "~/components/TaskTodo.vue";
export default {
  data() {
    return {
      newTodo: ""
    };
  },
  components: {
    TaskTodo
  },
  methods: {
    addTodo: function() {
      var value = this.newTodo && this.newTodo.trim();
      console.log(value);
    }
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
</style>
