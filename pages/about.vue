<template>
    <div class="about">
        <div class="container">
            <div class="about__description">
                <h1 class="about__title">What We Are All About</h1>
                <p>
                    It’s not always easy to filter out noise and purely focus on the content. Too many blogs and news sites are filled with colourful and distracting 
                    advertisement left right and centre. This is where we do things differently! Rather than just focusing purely and generating revenue, we focus 
                    on great user experience.   
                </p>
                <p>
                    You will notice that our news articles are content focused and free of any distractions. On top of that, we deliver content revolving design on a 
                    daily basis. Offering you insightful tutorials, techniques, design inspirations, mobile app development, coding, unique advertisements, and 
                    freebies.
                </p>
                <p>Our focus is and forever will be to bring high quality resources to lean from and to be inspired. Visit us daily for new design related articles!</p>
            </div>
            <div class="team">
                <h1 class="about__title">Meet Our Team!</h1>
                <div class="team__wrap">
                    <person/>
                    <person/>
                    <person/>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Person from '~/components/Person.vue'
export default {
  components: {
    Person
  }
}
</script>

<style lang="sass">
.about
    padding: 50px 0px
    &__title
        text-align: center
        margin-bottom: 50px
        font-size: 48px
        color: rgb(17, 17, 17)
    &__description
        margin-bottom: 50px
        p
            font-size: 16px
            color: rgb(17, 17, 17)
            line-height: 1.25
            margin-bottom: 30px
.team
    &__wrap
        display: flex
        flex-wrap: wrap
</style>
