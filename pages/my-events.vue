<script>
    export default {
        inject: ["userEventList"]
    }
</script>

<template>
    <div class="my-event__container">
        <MyEventsCard v-for="(e, index) in userEventList" :key=index :title=e.title :description=e.description />
    </div>
</template>

<style>
    .my-event__container {
        display: flex;
        flex-direction: column;
        gap: 24px;
    }
</style>