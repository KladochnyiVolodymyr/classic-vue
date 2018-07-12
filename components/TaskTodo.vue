<template>
    <li class="task">
        <input type="checkbox">
        <label class="task__title">Task</label>
    </li>
</template>
<script>
export default {
  data() {
    return {};
  }
};
</script>

<style lang="sass">
.task
    width: 500px
    border: 2px solid #999
    border-radius: 10px
    padding: 10px
    display: flex

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
</style>
