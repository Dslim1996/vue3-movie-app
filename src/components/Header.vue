<template>
    <header>
        <Logo />
        <div class="nav nav-pills">
            <div
            v-for="nav in navigatons"
            :key="nav.name" 
            class="nav-item">
                <RouterLink 
                :to="nav.href"
                active-class="active" 
                class="nav-link">
                    {{ nav.name}}
                </RouterLink>
            </div>
        </div>
    </header>
</template>

<script>
import Logo from "~/components/Logo"

export default {
    data() {
        return {
            navigatons: [
                {
                    name: 'Search',
                    href: '/'
                },

                {
                    name: 'movie',
                    href: '/movie/tt4520988'
                },

                {
                    name: 'about',
                    href: '/about'
                }
            ]
        }
    },
    components: {
        Logo
    }
}
</script>

<style lang="scss" scoped>
    header {
        height: 70px;
        padding: 0 40px;
        display: flex;
        align-items: center;
        .logo {
            margin-right: 40px;
        }
    }
</style>