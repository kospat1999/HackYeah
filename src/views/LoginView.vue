<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <main class="login-view">
    <h1 class="title">Yeah Bike App</h1>
    <p class="description">Odkryj miasto na dwóch kółkach</p>
    <RouterLink to="/home" class="login-button">Ruszaj w drogę</RouterLink>
  </main>
</template>

<style scoped lang="scss">
.login-view {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-end;
  gap: 12px;
  min-height: 100svh;
  padding: 24px;
  background-image: url('https://yeahbike.jurczak.dev/img/15.png');
  background-size: cover;

  .title {
    font:
      500 56px/44px 'Roboto',
      'sans-serif',
      'arial';
    color: #fff;
  }

  .description {
    font:
      400 16px/24px 'Roboto',
      'sans-serif',
      'arial';
    color: #fff;
  }

  .login-button {
    border: 1px solid #dadada;
    background-color: #f6f6f6;
    font:
      500 16px/24px 'Roboto',
      'sans-serif',
      'arial';
    border-radius: 40px;
    padding: 8px;
    width: 100%;
    min-width: 280px;
    align-items: center;
    justify-content: center;
    display: flex;
    color: #323232;
    position: relative;
    min-height: 64px;
    margin-top: 120px;

    &::before {
      content: url(../images/arrow-right.svg);
      background-color: #222222;
      padding: 12px;
      display: flex;
      right: 8px;
      position: absolute;
      border-radius: 50%;
      width: 48px;
      height: 48px;
    }
  }
}
</style>
