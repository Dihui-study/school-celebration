<template>
    <div class="home-index">
        <div class="home-index-1">
            <div></div>
            <div></div>
        </div>
        <div class="home-index-2">
            <div class="home-item">1</div>
            <div class="home-item">2</div>
            <div class="home-item">3</div>
        </div>
    </div>
</template>
<script lang="ts">
import { defineComponent, reactive } from 'vue'
export default defineComponent({
    name: 'home',
    components: {},
    setup() {}
})
</script>
<style lang="less" scoped>
.home-index {
    scroll-snap-type: y mandatory;
    height: 100vh;
    overflow: auto;
    &::-webkit-scrollbar {
        width: 0;
    }
    .home-index-1 {
        scroll-snap-align: start;
        width: 100%;
        height: 100vh;
        display: flex;
        align-items: center;
        justify-content: space-between;
        div {
            width: 50px;
            height: 50px;
            background: #000;
        }
    }
    .home-index-2 {
        // width: 100vw;
        height: 100vh;
        overflow: auto;
        scroll-snap-align: start;
        scroll-snap-type: y mandatory;

        .home-item {
            width: 100%;
            height: 100vh;
            font-size: 30px;
            display: flex;
            justify-content: center;
            align-items: center;
            scroll-snap-align: start;
        }

        .home-item:nth-child(1) {
            background-color: rgb(255, 255, 255);
        }

        .home-item:nth-child(2) {
            height: 200vh;
            background-color: rgb(137, 137, 137);
        }

        .home-item:nth-child(3) {
            background-color: rgb(50, 50, 50);
        }
    }
}
</style>
