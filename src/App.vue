<script lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HomeFooter from './components/HomeFooter.vue'
import HomeHeader from './components/HomeHeader.vue'
import { defineComponent } from 'vue'
export default defineComponent({
    components: {
        HomeHeader,
        HomeFooter
    },
    setup() {}
})
</script>

<template>
    <home-header />
    <main>
        <RouterView />
    </main>
    <home-footer />
</template>

<style scoped></style>
