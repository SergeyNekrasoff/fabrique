<template>
  <div class="container">
    <a-layout class="test-container" >
      <Sidebar />
      
      <a-layout class="test-container__inner">
        <Header />

        <a-layout-content class="test-content">
          <div class="test-content__inner">
            <nuxt />
          </div>
        </a-layout-content>
      </a-layout>
    </a-layout>
  </div>
</template>

<script>
const Header = () => import('~/components/base/header')
const Sidebar = () => import('~/components/base/sidebar')

export default {
  components: {
    Header,
    Sidebar
  }
}
</script>

<style lang="scss" scoped>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.test-container {
  background: #fff;
  position: relative;
  height: 100%;
  min-height: 100vh;

  &__inner {
    background: #fff;
  }
}

.test-content {
  margin: 24px 16px 0;

  &__inner {
    padding: 24px; 
    background: #fff;
    min-height: 360px;
  }
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
</style>
