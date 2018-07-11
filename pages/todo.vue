<template>
    <div class="container wrapper">
        <div class="todo">
            <h1 class="todo__title">TODO</h1>
            <input class="todo__new" placeholder="What needs to be done?">
            <ul class="todo__list">
                <li class="todo__item">
                    <input type="checkbox">
                    <label>Task</label>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    data () {
        return {
            
        }
    },
    components: {
        
    }
}
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
        padding: 10px
        margin-bottom: 10px
    &__list
        width: 500px
        display: inline-block
    &__item
        width: 500px
        border: 2px solid #999
        border-radius: 10px
        padding: 10px
        display: flex
</style>
