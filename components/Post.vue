<template>
    <div class="post">
        <h1 class="post__title">{{titlePost}}</h1>
        <span class="post__data">{{datePost}}</span>
        <img class="post__img" :src="imagePost">
        <p class="post__description">{{textPost}}</p>
        <button v-on:click="show = !show" class="post__more">Read more</button>
        <transition name="fade">  
            <div v-if="show">{{morePost}}</div>
        </transition>
    </div>
</template>
<script>
export default {
  data() {
    return {
      show: false
    };
  },
  props: ["titlePost", "datePost", "textPost", "morePost", "imagePost"]
};
</script>

<style lang="sass" scoped>
.post
    margin-bottom: 50px
    &__title
        text-align: center
        font-size: 48px
        color: rgb(17, 17, 17)
        max-width: 710px
        margin: 0 auto
    &__data
        text-align: center
        display: block
        font-size: 14px
        color: rgb(119, 119, 119)
        line-height: 3.571
    &__img
        display: block
        margin: 0 auto
        margin-bottom: 20px
    &__description
        margin-bottom: 20px
        font-size: 16px
        color: rgb(17, 17, 17)
        line-height: 1.25
    &__more
        font-size: 16px
        color: rgb(17, 17, 17)
        font-weight: bold
        background: none
        margin-bottom: 20px
.fade-enter-active, .fade-leave-active 
  transition: all 0.25s ease-out
.fade-enter, .fade-leave-to 
  opacity: 0
  transform: translate(100px, 0px)
</style>
