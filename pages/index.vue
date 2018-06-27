<template>
  <div>
    <div class="container">
      <div class="posts" v-for="post in posts" :key="post.id">
        <post :title-post="post.title" :date-post="post.date" :text-post="post.text" :more-post="post.moreText" />
      </div>
    </div>
  </div>
</template>

<script>
import Post from '~/components/Post.vue'
export default {
  data () {
    return {
      posts:[
        {
          title: 'Our Favourite Task Management App!',
          date: 'Posted on March 28, 2013',
          text: '6Wunderkinder’s flagship product, Wunderlist, has been a massive hit since its inception. Arguably one of the best to manage your tasks in your business and personal life. What makes it different from any other app? Simplicity. You don’t need to fiddle around with so many unnecessary features like you would with traditional to-do apps. Soon as you open the app, Wunderlist dives right into your tasks and you can get to work.',
          moreText: '6Wunderkinder’s flagship product,Wunderlist, has been a massive hit since its inception. Arguably one of the best to manage your tasks in your business and personal life'
        },
        {
          title: 'Our Favourite Task Management App!',
          date: 'Posted on March 28, 2013',
          text: '6Wunderkinder’s flagship product, Wunderlist, has been a massive hit since its inception. Arguably one of the best to manage your tasks in your business and personal life. What makes it different from any other app? Simplicity. You don’t need to fiddle around with so many unnecessary features like you would with traditional to-do apps. Soon as you open the app, Wunderlist dives right into your tasks and you can get to work.',
          moreText: '6Wunderkinder’s flagship product,Wunderlist, has been a massive hit since its inception. Arguably one of the best to manage your tasks in your business and personal life'
        },
        {
          title: 'Our Favourite Task Management App!',
          date: 'Posted on March 28, 2013',
          text: '6Wunderkinder’s flagship product, Wunderlist, has been a massive hit since its inception. Arguably one of the best to manage your tasks in your business and personal life. What makes it different from any other app? Simplicity. You don’t need to fiddle around with so many unnecessary features like you would with traditional to-do apps. Soon as you open the app, Wunderlist dives right into your tasks and you can get to work.',
          moreText: '6Wunderkinder’s flagship product,Wunderlist, has been a massive hit since its inception. Arguably one of the best to manage your tasks in your business and personal life'
        }
      ]
    }
  },
  components: {
    Post
  },
}
</script>

<style lang="sass">
.posts
  padding: 50px 0px
</style>
