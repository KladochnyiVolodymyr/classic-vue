<template>
    <header class="header">
        <div class="container">
            <div class="header__inner">
                <div class="header__logo">
                    <router-link to="/" class="logo">Classic</router-link>
                </div>
                <div class="header__nav">
                    <ul class="nav">
                        <li>
                            <router-link to="/">Home</router-link>
                        </li>
                        <li>
                            <router-link to="about">About</router-link>
                        </li>
                        <li>
                            <router-link to="todo">TODO</router-link>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>


<style lang="sass">
.header
    background: #111
    padding: 25px 0px
    &__inner
        display: flex
        justify-content: space-between
        align-items: center
.nav
    display: flex
    li
        margin-left: 30px
    a
        text-decoration: none
        color: rgb(255, 255, 255)
        font-size: 16px
        text-transform: uppercase

.logo
  font-size: 24px
  color: rgb(255, 255, 255)
  text-decoration: none
</style>
