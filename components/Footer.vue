<template>
    <div class="footer">
        <div class="footer__content">
            <p class="footer__text">DIM0536 - TÓPICOS ESPECIAIS EM ENGENHARIA DE SOFTWARE VI</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Footer'
    }
</script>

<style scoped>
    .footer {
        width: 100%;
        height: 80px;
        background-color: var(--blue-hover);
        color: #fff;
        display: flex;
        margin-top: 40px;
    }
    .footer__content {
        width: 100%;
        max-width: 1200px;
        margin: 0 auto;
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>