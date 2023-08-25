<template>
    <div class="school-header school-header-animation-up">herasdasd</div>
</template>

<script lang="ts">
import { defineComponent, watch } from 'vue'
export default defineComponent({
    name: 'home',
    components: {},
    setup() {
        watch(
            () => document.getElementById('#app')?.scrollHeight,
            (val) => {
                console.log('val:', val)
            }
        )
    }
})
</script>

<style lang="less" scoped>
.school-header {
    position: fixed;
    top: 0;
    width: 100vw;
    height: 80px;
    background: #dff;
}
.school-header-animation-down {
    animation-name: headerHidden;
    animation-timing-function: linear;
    animation-duration: 1s;
}
.school-header-animation-up {
    animation-name: headerShow;
    animation-timing-function: linear;
    animation-duration: 1s;
}
@keyframes headerHidden {
    0% {
        top: 0px;
    }
    25% {
        top: -40px;
    }
    50% {
        top: -80px;
    }
    75% {
        background: red;
        top: -40px;
    }
    100% {
        top: 0px;
    }
}
@keyframes headerShow {
    0% {
        top: 0;
    }
    25% {
        top: -40px;
    }
    50% {
        top: -80px;
    }
    75% {
        background: #dff;
        top: -40px;
    }
    100% {
        top: 0;
    }
}
</style>
