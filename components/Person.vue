<template>
    <div class="person">
        <div class="person__img"></div> 
        <h3 class="person__name">Kimberly Thompson</h3>
        <span class="person__position">Founder & CEO</span>
        <p class="person__description">Kimberly is the founder and the CEO of our company. With 10 years of experience in the tech industry, she ensures all operations are running smoothly.</p>
    </div>
</template>
<script>

</script>

<style lang="sass">
.person
    width: calc(100% / 3)
    margin-bottom: 50px
    text-align: center
    &__img
        width: 150px
        height: 150px
        background: #000
        border-radius: 50%
        margin: 0px auto
    &__name
        margin-bottom: 10px
        margin-top: 30px
    &__position
        display: block
        margin-bottom: 20px
</style>
