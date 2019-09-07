<template>
  <div>
    <div class="menu-back" v-if="!isRoute">
      <a @click="back">←back</a>
    </div>
    <div class="container">
      <nuxt />
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    isRoute() {
      return this.$route.path === '/'
    }
  },
  methods: {
    back() {
      this.$router.push('/')
    }
  }
}
</script>
<style>
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

h2 {
  margin: 28px;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  text-align: center;
}

.menu-back {
  padding: 20px;
}

.menu-back a {
  cursor: pointer;
  font-size: 1.3rem;
}

.form-container {
  width: 900px;
}
.editor {
  text-align: left;
  border: 4px solid #71c79e;
}
</style>
