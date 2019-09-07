<template>
  <div class="form-container">
    <div>
      <h1 class="title">wysiwyg-sample</h1>
      <ul class="menu-container">
        <nuxt-link to="/editorjs">Editor.js</nuxt-link>
        <nuxt-link to="/quill">Quill</nuxt-link>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.form-container {
  display: flex;
  justify-content: center;
  text-align: center;
  align-items: center;
}
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 40px;
  color: #35495e;
  letter-spacing: 1px;
  margin-bottom: 40px;
}

.menu-container {
  margin: 20px;
}
.menu-container a {
  display: block;
  font-size: 1.3rem;
  padding-bottom: 16px;
}
</style>
