<template>
  <div class="wrapper">
    <div class="container">
      <input class="search" type="text" placeholder="Search" v-model="search">
      <div class="posts">
        <post v-for="post in filteredPosts" :key="post.id" :title-post="post.title" :date-post="post.date" :text-post="post.text" :more-post="post.moreText" :image-post="post.imagePost" />
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
          text: 'Wunderkinder’s flagship product, Wunderlist, has been a massive hit since its inception. Arguably one of the best to manage your tasks in your business and personal life. What makes it different from any other app? Simplicity. You don’t need to fiddle around with so many unnecessary features like you would with traditional to-do apps. Soon as you open the app, Wunderlist dives right into your tasks and you can get to work.',
          moreText: 'Wunderkinder’s flagship product,Wunderlist, has been a massive hit since its inception. Arguably one of the best to manage your tasks in your business and personal life',
          imagePost: '/logo.png'
        },
        {
          title: 'Year in Review: Our Favourite Apps from 2012',
          date: 'Posted on March 28, 2013',
          text: 'Wunderkinder’s flagship product, Wunderlist, has been a massive hit since its inception. Arguably one of the best to manage your tasks in your business and personal life. What makes it different from any other app? Simplicity. You don’t need to fiddle around with so many unnecessary features like you would with traditional to-do apps. Soon as you open the app, Wunderlist dives right into your tasks and you can get to work.',
          moreText: 'Wunderkinder’s flagship product,Wunderlist, has been a massive hit since its inception. Arguably one of the best to manage your tasks in your business and personal life',
          imagePost: '/logo.png'
        },
        {
          title: 'Marketing Tips & Tricks From the Top Brands',
          date: 'Posted on March 28, 2013',
          text: 'Wunderkinder’s flagship product, Wunderlist, has been a massive hit since its inception. Arguably one of the best to manage your tasks in your business and personal life. What makes it different from any other app? Simplicity. You don’t need to fiddle around with so many unnecessary features like you would with traditional to-do apps. Soon as you open the app, Wunderlist dives right into your tasks and you can get to work.',
          moreText: 'Wunderkinder’s flagship product,Wunderlist, has been a massive hit since its inception. Arguably one of the best to manage your tasks in your business and personal life',
          imagePost: '/logo.png'
        }
      ],
      search:""
    }
  },
  components: {
    Post
  },
  computed: {
    filteredPosts: function(){
      return this.posts.filter((post) => {
        return post.title.toLowerCase().includes(this.search.toLowerCase())
      });
    }
  }
}
</script>

<style lang="sass">
.wrapper
   min-height: calc(100vh - 150px)
.posts
  padding: 50px 0px
.search
  border: 2px solid #999
  width: 500px
  display: block
  margin: 0 auto
  border-radius: 10px
  height: 40px
  margin-top: 20px
  padding: 0px 20px
</style>
