<template>
  <div>
    <header class="m-header">
      <div class="header-bar">
        <LoginRegister></LoginRegister>
      </div>
    </header>
    <nuxt/>
  </div>
</template>
<script>
  import LoginRegister from '../components/commonHeader/Login-register'

  export default {
    components: {
      LoginRegister
    }
  }
</script>
<style lang="less">
  html {
    font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
    font-size: 16px;
    word-spacing: 1px;
    -ms-text-size-adjust: 100%;
    -webkit-text-size-adjust: 100%;
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    box-sizing: border-box;
  }

  *,
  *:before,
  *:after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  html, body {
    width: 100%;
    height: 100%;
    background: #f8f8f8;
  }

  li {
    list-style: none;
  }

  a {
    text-decoration: none;
    color: #999999;
  }

  .m-header {
    width: 100%;
    height: 197px;
    background: #ffffff;
    box-shadow: 0 2px 27px 0 rgba(0, 0, 0, .1);
    .header-bar {
      font-size: 12px;
      background: #f8f8f8;
      color: #666;

    }
  }

</style>
