<template>
  <div class="wrapper">
    <div class="sidebar">
      <div class="sidebar__item">
        <router-link to="/">Home</router-link>
      </div>
      <div class="sidebar__item">
        <router-link to="/about">About</router-link>
      </div>
       <div class="sidebar__item">
        <router-link to="/signin">Sign in</router-link>
      </div>
    </div>
    <div class="content">
      <router-view />
    </div>
  </div>
</template>

<style lang="scss">
* {
  margin: 0;
  box-sizing: border-box;
}

#app {
  color: #3b3b3b;
}

.wrapper {
  display: flex;
  padding: 15px;
  min-height: 100vh;
  background: #3b3b3b;
}
.sidebar {
  padding: 15px;
  width: 15%;
  margin-right: 15px;
  border-radius: 15px;
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: #ffffff;

  & a {
    font-weight: bold;
    color: #3b3b3b;
    text-decoration: none;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
  &__item {
    padding-top: 10px;
    padding-bottom: 10px;
  }
}

.content {
  width: 85%;
  border-radius: 15px;
  background: #ffffff;
}
</style>
