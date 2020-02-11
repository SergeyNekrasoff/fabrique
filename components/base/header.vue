<template>
  <header class="header">
    <a-row class="header__top" justify="space-between">
      <a-col :xl="18">
        <a-input-search placeholder="Поиск по системе" @search="onSearch" />
        </a-col>
      <a-col :xl="6">
        <div class="profile">
          <a-avatar 
            class="avatar"
            src="https://zos.alipayobjects.com/rmsportal/ODTLcjxAfvqbxHnVXCYX.png" />
          <div class="profile__info">
            <div class="profile__name">{{ `Alexander C.` }}</div>
            <div class="profile__role">{{ `Администратор` }}</div>
          </div>
        </div>
      </a-col>
    </a-row>
    <a-row class="header__bottom">
      <a-col :xl="24">
        <!-- <a-breadcrumb separator="➔">
          <a-breadcrumb-item href="/">
            <a-icon type="home" />
          </a-breadcrumb-item>
          <a-breadcrumb-item 
            :href="`/${$route.name}`">
            <span>{{ crumbs.find(crumb => crumb.name === $route.name).description }}</span>
          </a-breadcrumb-item>
        </a-breadcrumb> -->
      </a-col>
    </a-row>
  </header>
</template>

<script>
export default {
  data() {
    return {
      crumbs: [
        {
          name: 'index',
          description: 'Главная'
        },
        {
          name: 'quiz',
          description: 'Опросы'
        },
        {
          name: 'users',
          description: 'Пользователи'
        },
        {
          name: 'blacklist',
          description: 'Черные списки'
        },
        {
          name: 'callcenter',
          description: 'Колл-центр'
        },
      ]
    }
  },
  methods: {
    onSearch(value) {
      console.log(value)
    }
  }
}
</script>

<style lang="scss" scoped>
.header {
  background: '#fff';
  padding: 0;
  text-align: left;

  &__top,
  &__bottom {
    padding: 20px 40px;
  }
}

.profile {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  flex-direction: row;
  text-align: right;

  .avatar {
    background: #ccc;
  }

  &__info {
    text-align: left;
    padding-left: 8px;
  }
  
  &__name {
    font-size: 14px;
    line-height: 15px;
    color: #333;
    font-weight: 600;
  }

  &__role {
    font-size: 12px;
    color: #999;
    font-weight: 300;
  }
}
</style>