<script>
    export default {
        props: {
            title: {
                type: String,
                required: true,
                default: "Event Name!"
            },
            description: {
                type: String,
                required: true,
                default: "Event Description."
            }
        }
    }
</script>

<template>
    <div class="my-event__card">
        <div class="my-event__picture"></div>
        <span class="my-event__data">
            <h1 class="my-event__title">{{ title }}</h1>
            <p class="my-event__description">{{ description }}</p>
        </span>
        <button class="my-event__unsubscribe">UNSUBSCRIBE</button>
    </div>
</template>

<style>
    .my-event__card {
        background-color: #fff;
        filter: drop-shadow(0 8px 15px rgba(0,0,0,.2));
        display: flex;
        position: relative;
    }
    .my-event__picture {
        background-image: url('../assets/nuxtjs.jpeg');
        background-size: cover;
        background-position: center;
        height: 220px;
        width: 220px;
        align-items: center;
    }
    .my-event__data {
        margin-left: 16px;
        display: flex;
        justify-content: center;
        flex-direction: column;
    }
    .my-event__unsubscribe {
        background-color: red;
        color: white;
        padding: 12px 16px;
        border: none;
        justify-self: flex-end;
        align-self: flex-end;
        position: absolute;
        right: 20px;
        bottom: 20px;
        transition: 150ms ease-in;
        cursor: pointer;
    }
    .my-event__unsubscribe:hover {
        background-color: rgb(121, 30, 30);
        filter: drop-shadow(0 5px 15px rgba(0,0,0,.15));
    }
</style>