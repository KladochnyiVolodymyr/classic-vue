<template>
    <footer class="footer">
        <div class="container">
            <div class="footer__inner">
                <ul class="footer__nav">
                    <li>
                        <router-link to="/">Home</router-link>
                    </li>
                    <li>
                        <router-link to="/">About</router-link>
                    </li>
                    <li>
                        <router-link to="/">Archive</router-link>
                    </li>
                    <li>
                        <router-link to="/">Contact</router-link>
                    </li>
                </ul>
                <div class="footer__social">
                </div>
                <span class="footer__copyright">
                    © Copyright 2013 DesignerFirst.com
                </span>
            </div>
        </div>
    </footer>
</template>


<style lang="sass">
.footer
    &__inner
        display: flex
        justify-content: space-between  
        border-top: 1px solid #999
        padding: 15px 0px
    &__nav
        display: flex
        li
            margin-right: 30px
        a
            text-decoration: none
            color: #555
    &__copyright
        font-size: 14px
        color: rgb(85, 85, 85)
    &__social
        img
            width: 40px
            height: 40px
</style>
