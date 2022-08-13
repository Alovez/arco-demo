<template>
    <VueDragResize :isActive="true" :w="200" :h="200" v-on:resizing="resize" v-on:dragging="resize">
        <h3>Hello World!</h3>
        <p>{{ top }} х {{ left }} </p>
        <p>{{ width }} х {{ height }}</p>
    </VueDragResize>
</template>

<script>
    import VueDragResize from 'vue-drag-resize';

    export default {

        components: {
            VueDragResize
        }
    }
</script>