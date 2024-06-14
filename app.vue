<template>
  <div>
    <AppHeader/>
    <section class="main__section">
      <div class="main__content">
          <NuxtPage />
      </div>
    </section>
    <Footer />
  </div>
</template>

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

<style>
  :root {
    --sign-up-blue: #1e88e5;
    --blue-hover: #024e90;
    --orange: #fca404;
  }
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: sans-serif;
  }
  html, body {
    min-height: 100lvh;
    width: 100vw;
    background-color: #fff;
  }
  #__nuxt, #__nuxt > div {
    display: flex;
    flex-direction: column;
    min-height: 100lvh;
  }
  .main__section {
    flex-grow: 1;
  }
  .main__content {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    margin-top: 40px;
  }
</style>
