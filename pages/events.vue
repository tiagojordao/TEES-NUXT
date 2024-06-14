<script>
    import events from '~/static/mock-data/events.json';

    export default {
        data() {
            return {
                events
            }
        }
    }
</script>


<template>
    <h1 class="events__title">EVENTS</h1>
    <div class="events__grid">
        <CardEvent v-for="(e, index) in events" :key="index" :title=e.title :description=e.description />
    </div>
</template>


<style scoped>
    .events__title {
        color: var(--blue-hover);
        margin-bottom: 20px;
    }
    .events__grid {
        width: 100%;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-gap: 2rem;
        justify-items: center;
    }
</style>
