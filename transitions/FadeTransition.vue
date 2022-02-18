<template>
    <transition name="fade" :mode="mode">
        <slot></slot>
    </transition>
</template>

<script>
    export default {
        name: "FadeTransition",
        props: {
            mode: {
                type: String,
            }
        }
    }
</script>

<style scoped>
    .fade-enter-active, .fade-leave-active {
        transition: opacity .3s;
    }

    .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */
    {
        opacity: 0;
    }
</style>
