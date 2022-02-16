<template>
    <div class="container mx-auto max-w-screen-lg xl:max-w-screen-2xl" :class="classes">
        <slot></slot>
    </div>
</template>

<script>
    export default {
        name: "Container",
        props: {
            isFluid: {
                type: Boolean,
                default: false,
            }
        },
        computed: {
            classes() {
                return {
                    'px-4': !this.isFluid,
                }
            }
        }
    }
</script>

<style scoped>

</style>
