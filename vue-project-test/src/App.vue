<template>
  <div id="app">
    <!-- Интерполяция текста -->
    <span class="username">{{ username }}</span>

    <!-- Сырой HTML -->
    <p><span v-html="htmlString"></span></p>

    <!-- Атрибуты -->
    <button v-bind:style="btnStyle">Кнопка</button>
    <button v-bind:disabled="isDisabled">Кнопка</button>

    <!-- Выражения Javascript -->
    {{ num + 1}}
    {{ isLoading ? 'Loading ...':'is loaded'}}
    {{ message.split('').reverse().join('')}}

    <!-- Директивы -->
    <!-- СОздает динамические атрибуты -->
    <!-- v-bind:href="itemUrl" -->
    <!-- v-bind:id="itemId" -->
    <!-- v-bind = : -->

    <!-- v-on = @ -->
    <!-- Обработчик событий -->
    <!-- v-on:click="getData" -->
    <!-- v-on:click.stop.prevent="submitForm" -->

    <!-- v-model -->
    <!-- СОздание двусторонней привязки HTML элементов -->

    <!-- v-show -->
    <!-- показать/скрыть элемент -->

    <!-- v-if -->
    <!-- Условие показа/скрытия элемента -->

    <!-- v-else -->
    <!-- v-else-if -->

    <!-- v-for -->
    <!-- Отрисовка списка элементов -->




    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
