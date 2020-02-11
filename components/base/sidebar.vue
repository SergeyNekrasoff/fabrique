<template>
  <a-layout-sider breakpoint="lg" class="sidebar">
    <nuxt-link to="/">
      <div class="logo" />
    </nuxt-link>
    
    <a-menu mode="inline">
      <a-menu-item key="1">
        <a-icon type="profile" />
        <span class="nav-text">
          <nuxt-link class="nav-link" to="/quiz">
            Опросы
          </nuxt-link>
        </span>
      </a-menu-item>
      <a-menu-item key="2">
        <a-icon type="team" />
        <span class="nav-text">
          <nuxt-link class="nav-link" to="/users">
            Пользователи
          </nuxt-link>
        </span>
      </a-menu-item>
      <a-menu-item key="3">
        <a-icon type="exception" />
        <span class="nav-text">
          <nuxt-link class="nav-link" to="/blacklist">
            Черные списки
          </nuxt-link>
        </span>
      </a-menu-item>
      <a-menu-item key="4">
        <a-icon type="phone" />
        <span class="nav-text">
          <nuxt-link class="nav-link" to="/callcenter">
            Колл-центр
          </nuxt-link>
        </span>
      </a-menu-item>
    </a-menu>
  </a-layout-sider>
</template>

<style lang="scss" scoped>
.sidebar {
  background: #fff; 
  box-shadow: inset 0px 0px 2px 0px #ccc;
  text-align: left;
}

.logo {
  background: tomato;
  width: 45px;
  height: 45px;
  margin: 25px auto;
  border-radius: 50%;
}

.nav-link {
  text-decoration: none;
  color: #333;

  &.nuxt-link-active {
    color: #1890ff;
  }
}
</style>