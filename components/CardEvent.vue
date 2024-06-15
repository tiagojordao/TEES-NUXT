<template>
    <div class="card">
        <div class="card__image"/>
        <div class="card__data">
            <h2 class="card__title">
                {{ title }}
            </h2>
            <h3 class="card__subtitle">
                {{ description }}
            </h3>
            <button @click="updateParent" class="card__button-sign-up" :class="{disabled: isDisabled}">
                SUBSCRIBE
            </button>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    title: {
      type: String,
      required: true,
      default: "Event Name"
    },
    description: {
      type: String,
      required: true,
      default: "Event description"
    }
  },
  inject: ['updateEvent'],
  methods: {
    updateParent() {
      this.updateEvent({
        title: this.title,
        description: this.description
      });
      this.isDisabled = true;
    }
  },
  data() {
    return {
      isDisabled: false
    }
  }
}
</script>

<style scoped>
    .card {
        background-color: #fff;
        width: 100%;
        max-width: 300px;
        filter: drop-shadow(0 3px 7px rgba(0,0,0,.2));
    }
    .card:hover {
        filter: brightness(.95) drop-shadow(0 3px 7px rgba(0,0,0,.2));
    }
    .card__image {
        background-image: url('../assets/nuxtjs.jpeg');
        background-size: cover;
        background-position: center;
        height: 200px;
    }
    .card__data {
        padding: 16px;
        display: flex;
        flex-direction: column;
    }
    .card__subtitle {
        font-weight: 300;
        color: #555;
    }
    .card__button-sign-up {
        background-color: var(--sign-up-blue);
        color: #fff;
        padding: 12px 20px;
        border: 1px solid #fff;
        margin-top: 12px;
        cursor: pointer;
        flex: 0;
        align-self: flex-end;
        transition: 175ms ease-in;
    }
    .card__button-sign-up:hover {
        background-color: var(--blue-hover);
        filter: drop-shadow(0 5px 10px rgba(0,0,0,.2));
    }
</style>