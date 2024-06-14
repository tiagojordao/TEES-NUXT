<script>
</script>


<template>
  <header class="header">
    <div class="header__content">
      <span class="header__logo">
        TEES
      </span>
      <nav class="header__nav">
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="/about">About</NuxtLink>
        <NuxtLink to="/events">Events</NuxtLink>
        <NuxtLink to="/contact">Support</NuxtLink>
      </nav>
      <span class="header__profile-container">
        <NuxtLink to="shopping-cart" class="header__shopping-cart-button">
          <img src="../assets/shoppingCart.png" alt="Shopping cart icon" class="header__shopping-cart-icon">
          <p class="header__shopping-cart-counter">5</p>
        </NuxtLink>
        <img src="../assets/userProfilePicture.jpeg" alt="Profile Picture" class="header__profile-picture">
      </span>
    </div>
  </header>
</template>

<style scoped>
  .header {
    width: 100%;
    display: flex;
  }
  .header__content {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    padding: 0 8px;
    border-bottom: 1px solid #bbb;
  }
  .header__logo {
    font-weight: bold;
    flex: 1;
    color: var(--blue-hover);
  }
  .header__nav {
    display: flex;
    align-items: center;
    gap: 8px;
    flex: 1;
    justify-content: center;
  }
  .header__nav > a {
    text-decoration: none;
    padding: 16px 4px;
    font-weight: 100;
    color: #555;
    border-bottom: 3px solid transparent;
    transition: 150ms ease-in-out border;
  }

  .header__nav > a:hover {
    color: #bbb;
    border-bottom: 3px solid orange;
  }

  .header__profile-container {
    flex: 1;
    display: flex;
    justify-content: flex-end;
    gap: 12px;
  }

  .header__profile-picture {
    width: 30px;
    height: 30px;
    border-radius: 50%;
  }

  .header__shopping-cart-button {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: transparent;
    border: none;
    cursor: pointer;
    transition: 150ms ease-in;
  }

  .header__shopping-cart-button:hover {
    transform: scale(1.1);
  }

  .header__shopping-cart-icon {
    width: 24px;
  }

  .header__shopping-cart-counter {
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
    width: 16px;
    height: 16px;
    background-color: red;
    border-radius: 50%;
    position: absolute;
    top: -5px;
    right: -10px;
    font-size: .8em;
  }
</style>
